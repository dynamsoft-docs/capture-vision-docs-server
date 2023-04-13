---
layout: default-layout
title: Capture Vision Router API Reference Index- Dynamsoft Capture Vision Router Module C++ Edition API Reference
description: This page is the index of the C++ edition API Reference of the Dynamsoft Capture Vision Router Module.
keywords: capture vision, router, c++, api reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: CVR C++ API Reference Index
permalink: /programming/cplusplus/api-reference/cvr/index.md
---

# Capture Vision Router C++ API Reference Index

The "Capture Vision Router" module is defined in the namespace `Dynamsoft.CVR` which consists of the main class `CCaptureVisionRouter` and a few enumerations and interfaces.

## CCaptureVisionRouter

The CCaptureVisionRouter class is what a user uses to interact with image-processing and semantic-processing products in their applications. It accepts an image source and returns processing results which may contain [Captured Results]() or [Intermediate Results]().

The APIs for this class include:

### Constructor and Destructor

| Method                                                              | Description                                           |
| ------------------------------------------------------------------- | ----------------------------------------------------- |
| [`CCapturedResultReceiver`](instantiate.md#ccapturevisionrouter)    | Default constructor of `CCaptureVisionRouter` object. |
| [`~CCapturedResultReceiver`](instantiate.md#ccapturevisionrouter-1) | Destructor of `CCaptureVisionRouter` object.          |

### Process a Single Image or File

| API Name                               | Description                                               |
| -------------------------------------- | --------------------------------------------------------- |
| [capture()](single-process.md#capture) | Process an image or file to derive important information. |


        // 从文件中进行Capture，考虑文件有可能多页，因此返回CCapturedResultArray
        // Note: 需要通过ISA实现
        CCapturedResultArray* Capture(const char* filePath, const char* templateName="");

        CCapturedResultArray* Capture(const unsigned char *fileBytes, int fileSize, const char* templateName="");

        // 从ImageData中进行Capture，返回CCapturedResult，表示一张图上的所有结果集合
        // Note: 需要通过ISA实现
        CCapturedResult* Capture(const CImageData* pImageData, const char* templateName="");


### Process multiple images from an Image Source

| API Name                                                                                | Description                                                                  |
| --------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| [setInput](consecutive-process.md#setinput)                                             | Sets an image source to provide images for consecutive process.              |
| [addCaptureStateListener()](consecutive-process.md#addcapturestatelistener)             | Adds an object that listens to the state changes of the capture process.     |
| [removeCaptureStateListener()](consecutive-process.md#removecapturestatelistener)       | Removes an object which listens to the state changes of the capture process. |
| [addImageSourceStateListener](consecutive-process.md#addimagesourcestatelistener)       | Adds an object that listens to state changes of the image source.            |
| [removeImageSourceStateListener](consecutive-process.md#removeimagesourcestatelistener) | Removes an object which listens to state changes of the image source.        |
| [addResultReceiver()](consecutive-process.md#addresultreceiver)                         | Adds an object as the receiver of captured results.                          |
| [removeResultReceiver()](consecutive-process.md#removeresultreceiver)                   | Removes an object which was added as a receiver of captured results.         |
| [startCapturing()](consecutive-process.md#startcapturing)                               | Starts to process images consecutively.                                      |
| [stopCapturing()](consecutive-process.md#stopcapturing)                                 | Stops the consecutive process.                                               |

### Change Settings

| API Name                                                     | Description                                                                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| [InitSettings()](settings.md#initsettings)                   | Initializes settings with a string.                                                                           |
| [InitSettingsFromFile()](settings.md#initsettingsfromfile)   | Initializes settings with a file.                                                                             |
| [OutputSettings](settings.md#outputsettings)                 | Outputs a `CaptureVisionTemplate` specified by its name as a string.                                          |
| [OutputSettingsToFile](settings.md#outputsettingstofile)     | Outputs a `CaptureVisionTemplate` specified by its name as a file.                                            |
| [GetSimplifiedSettings()](settings.md#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`.      |
| [UpdateSettings()](settings.md#updatesettings)               | Updates a specified `CaptureVisionTemplate` with updated an updated `SimplifiedCaptureVisionSettings` object. |
| [ResetSettings()](settings.md#resetsettings)                 | Resets settings to factory default.                                                                           |

### Auxiliary

| API Name                                      | Description                                                       |
| --------------------------------------------- | ----------------------------------------------------------------- |
| [getIntermediateResultManager](auxiliary.md#) | Whether to save the original image into a &lt;canvas&gt; element. |
| [getVersion](auxiliary.md#getVersion)         |                                                                   |

## Interfaces and Enums

In order to make the code more predictable and readable, the library defines a series of supporting interfaces and enumerations:

### Interfaces

* [CapturedResultReceiver](interfaces/captured-result-receiver.md)
* [CaptureStateListener](interfaces/capture-state-listener.md)
* [ImageSourceStateListener](interfaces/image-source-state-listener.md)
* [RawImageResultItem](interfaces/raw-image-result-item.md)
* [SimplifiedCaptureVisionSettings](interfaces/simplified-capture-vision-settings.md)

### Enums

* [EnumImageSourceState](enums/image-source-state.md)
* [EnumCaptureState](enums/capture-state.md)

        // 注册CImageSourceAdapter
        void SetInput(CImageSourceAdapter* pAdaptor);
        
        // void SetImageSourceAdapterStateCallback(ImageSourceAdapterStateCallback callback, void* userArgs = NULL);
        
        //// 设置Captured result回调函数
        // void SetOutput(CapturedResultCallback callbackFunc, void* userArgs=NULL);
        void AddImageSourceStateListener(CImageSourceStateListener* listener);
        void RemoveImageSourceStateListener(CImageSourceStateListener* listener);

        void AddResultReceiver(CCapturedResultReceiver* receiver);
        void RemoveResultReceiver(CCapturedResultReceiver* receiver);

        void AddCaptureStateListener(CCaptureStateListener* listener);
        void RemoveCaptureStateListener(CCaptureStateListener* listener);
        //void SetCaptureStateCallback(CaptureStateCallback callbackFunc, void* userArgs=NULL);

        // 启动Caputring, 每处理一张图都会回调一次
        // waitForCompletion = true：调用后不会返回，而是等待结束标志
        // waitForCompletion = false：调用后立即返回，不会等待结束标志
        // Error处理:
        // 1)DBR/DLR/DDN模板延迟解析：模块不存在；模板有错误；
        // 2)License与模板的匹配判断：模板Task所需模块的License超出已有License授权的模板
        int StartCapturing(const char* templateName = "", bool waitForCompletion = false, char errorMsgBuffer[]=NULL, const int errorMsgBufferLen=0);

        // 停止Caputring
        // waitForCompletion = true：调用后等待任务队列执行完毕才停止
        // waitForCompletion = false：调用后清空剩余任务队列，立即停止
        void StopCapturing(bool waitForCompletion = true);

        static const char* GetVersion();
        static void FreeString (char* content);

        // 获得中间结果管理器，在该接口中注册回调函数，以便监听各个层面的中间结果回调
        CIntermediateResultManager* GetIntermediateResultManager();

    private:
        CCaptureVisionRouter(const CCaptureVisionRouter& r);
        CCaptureVisionRouter& operator=(const CCaptureVisionRouter& r);
    };





namespace cvr {
    
    class CVR_API CCaptureStateListener
    {
    public:
        virtual void OnCaptureStateChanged(CaptureState state) = 0;
    };

    class CVR_API CImageSourceStateListener
    {
    public:
        virtual void OnImageSourceStateChanged(ImageSourceState state) = 0;
    };

    class CVR_API CCapturedResultReceiver
    {
    protected:
        unsigned int observedResultItemTypes;

    public:
        CCapturedResultReceiver();
        virtual ~CCapturedResultReceiver();
        
        unsigned int GetObservedResultItemTypes(); 

        /**
         * @brief 所有结果的回调，一张图回调一次
         * 1.每一个基类回调函数实现解除对自身的监听（OnCapturedResultReceived除外）：譬如observedResultItemTypes = observedResultItemTypes & (~CRIT_BARCODE)
         * 2.OnCapturedResultReceived无论pResult是否为NULL，均会回调；其余callback只有当非NULL时才有可能回调
         */
        virtual void OnCapturedResultReceived(const CCapturedResult* pResult);

        /**
         * @brief 原图结果的回调，一张图回调一次
         */
        virtual void OnRawImageResultReceived(const CRawImageResultItem* pResult);

        /**
         * @brief 所有Barcode结果的回调，一张图回调一次
         */
        virtual void OnDecodedBarcodesReceived(const dbr::CDecodedBarcodesResult* pResult);

        /**
         * @brief 所有TextLine结果的回调，一张图回调一次
         */
        virtual void OnRecognizedTextLinesReceived(const dlr::CRecognizedTextLinesResult* pResult);

        /**
         * @brief 所有DetectedQuads结果的回调，一张图回调一次
         */
        virtual void OnDetectedQuadsReceived(const ddn::CDetectedQuadsResult* pResult);

        /**
         * @brief 所有NormalizedImage结果的回调，一张图回调一次
         */
        virtual void OnNormalizedImagesReceived(const ddn::CNormalizedImagesResult* pResult);

        /**
         * @brief 所有ParsedResult结果的回调，一张图回调一次
         */
        virtual void OnParsedResultsReceived(const dcp::CParsedResult* pResult);

    };
    
    class CVR_API CRawImageResultItem: public CCapturedResultItem
    {
    public:
        virtual ~CRawImageResultItem(){};
        virtual const CImageData* GetImageData() const = 0;
    };

    

} 
}
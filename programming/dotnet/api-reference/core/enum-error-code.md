---
layout: default-layout
title: ErrorCode - Dynamsoft Core .NET Enumerations
description: The enumeration ErrorCode describes all error codes for .NET Edition.
keywords: Error code
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
codeAutoHeight: true
---

# Enumeration ErrorCode

`ErrorCode` enumerates the specific error codes that the SDK may return, providing a systematic way to identify and handle errors encountered during its operation.

```csharp
public enum EnumErrorCode
{
    /** Successful. */
    EC_OK = 0,
    /** -10000~-19999: Common error code. */
    /** Unknown error. */
    EC_UNKNOWN = -10000,
    /**Not enough memory to perform the operation. */
    EC_NO_MEMORY = -10001,
    /** Null pointer */
    EC_NULL_POINTER = -10002,
    /** License invalid. */
    EC_LICENSE_INVALID = -10003,
    /** License expired. */
    EC_LICENSE_EXPIRED = -10004,
    /** File not found. */
    EC_FILE_NOT_FOUND = -10005,
    /** The file type is not supported. */
    EC_FILE_TYPE_NOT_SUPPORTED = -10006,
    /** The BPP (Bits Per Pixel) is not supported. */
    EC_BPP_NOT_SUPPORTED = -10007,
    /** The index is invalid. */
    EC_INDEX_INVALID = -10008,
    /** The input region value parameter is invalid. */
    EC_CUSTOM_REGION_INVALID = -10010,
    /** Failed to read the image. */
    EC_IMAGE_READ_FAILED = -10012,
    /** Failed to read the TIFF image. */
    EC_TIFF_READ_FAILED = -10013,
    /** The DIB (Device-Independent Bitmaps) buffer is invalid. */
    EC_DIB_BUFFER_INVALID = -10018,
    /** Failed to read the PDF image. */
    EC_PDF_READ_FAILED = -10021,
    /** The PDF DLL is missing. */
    EC_PDF_DLL_MISSING = -10022,
    /** The page number is invalid. */
    EC_PAGE_NUMBER_INVALID = -10023,
    /** The custom size is invalid. */
    EC_CUSTOM_SIZE_INVALID = -10024,
    /** timeout. */
    EC_TIMEOUT = -10026,
    /** Json parse failed. */
    EC_JSON_PARSE_FAILED = -10030,
    /** Json type invalid. */
    EC_JSON_TYPE_INVALID = -10031,
    /** Json key invalid. */
    EC_JSON_KEY_INVALID = -10032,
    /** Json value invalid. */
    EC_JSON_VALUE_INVALID = -10033,
    /** Json name key missing. */
    EC_JSON_NAME_KEY_MISSING = -10034,
    /** The value of the key "Name" is duplicated. */
    EC_JSON_NAME_VALUE_DUPLICATED = -10035,
    /** Template name invalid. */
    EC_TEMPLATE_NAME_INVALID = -10036,
    /** The name reference is invalid. */
    EC_JSON_NAME_REFERENCE_INVALID = -10037,
    /** Parameter value invalid. */
    EC_PARAMETER_VALUE_INVALID = -10038,
    /** The domain of your current site does not match the domain bound in the current product key. */
    EC_DOMAIN_NOT_MATCH = -10039,
    /** The license key does not match the license content. */
    EC_LICENSE_KEY_NOT_MATCH = -10043,
    /** Failed to set mode's argument. */
    EC_SET_MODE_ARGUMENT_ERROR = -10051,
    /** Failed to get mode's argument. */
    EC_GET_MODE_ARGUMENT_ERROR = -10055,
    /** The Intermediate Result Types license is invalid. */
    EC_IRT_LICENSE_INVALID = -10056,
    /** Failed to save file. */
    EC_FILE_SAVE_FAILED = -10058,
    /** The stage type is invalid. */
    EC_STAGE_TYPE_INVALID = -10059,
    /** The image orientation is invalid. */
    EC_IMAGE_ORIENTATION_INVALID = -10060,
    /** Complex tempalte can't be converted to simplified settings. */
    EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
    /** Reject function call while capturing in progress.*/
    EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
    /**The input image source was not found.*/
    EC_NO_IMAGE_SOURCE = -10063,
    /**Failed to read directory.*/
    EC_READ_DIRECTORY_FAILED = -10064,
    /**[Name] Module not found.*/
    /**Name : */
    /**DynamsoftBarcodeReader*/
    /**DynamsoftLabelRecognizer*/
    /**DynamsoftDocumentNormalizer*/
    EC_MODULE_NOT_FOUND = -10065,
    //The api does not support multi-page files. Please use CaptureMultiPages instead.
    EC_MULTI_PAGES_NOT_SUPPORTED = -10066,
    /**The file already exists but overwriting is disabled.*/
    EC_FILE_ALREADY_EXISTS = -10067,
    /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
    EC_CREATE_FILE_FAILED = -10068,
    /**The input ImageData object contains invalid parameter(s).*/
    EC_IMGAE_DATA_INVALID = -10069,
    /**The size of the input image do not meet the requirements.*/
    EC_IMAGE_SIZE_NOT_MATCH = -10070,
    /**The pixel format of the input image do not meet the requirements.*/
    EC_IMAGE_PIXEL_FORMAT_NOT_MATCH = -10071,
    /**The section level result is irreplaceable.*/
    EC_SECTION_LEVEL_RESULT_IRREPLACEABLE = -10072,
    /**The axis definition is incorrect.*/
    EC_AXIS_DEFINITION_INCORRECT = -10073,
    /**The result is not replaceable due to type mismatch*/
    EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE = -10074,
    /**Failed to load the PDF library.*/
    EC_PDF_LIBRARY_LOAD_FAILED = -10075,
    /**The license is initialized successfully but detected invalid content in your key.*/
    EC_LICENSE_WARNING = -10076,
    /*One or more unsupported JSON keys were encountered and ignored from the template.*/
    EC_UNSUPPORTED_JSON_KEY_WARNING = -10077,
    /**Model file is not found*/
    EC_MODEL_FILE_NOT_FOUND = -10078,
    /**[PDF] No license found.*/
    EC_PDF_LICENSE_NOT_FOUND = -10079,
    /**The rectangle is invalid.*/
    EC_RECT_INVALID = -10080,
    /*The template version is incompatible. Please use a compatible template.*/
    EC_TEMPLATE_VERSION_INCOMPATIBLE = -10081,
    /**The portrait zone could not be located on the identity document.*/
    EC_PORTRAIT_ZONE_NOT_FOUND = -10082,
    /** -20000~-29999: DLS license error code. */
    /** No license. */
    EC_NO_LICENSE = -20000,
    /** The Handshake Code is invalid. */
    EC_HANDSHAKE_CODE_INVALID = -20001,
    /** Failed to read or write license buffer. */
    EC_LICENSE_BUFFER_FAILED = -20002,
    /** Failed to synchronize license info with license server. */
    EC_LICENSE_SYNC_FAILED = -20003,
    /** Device dose not match with buffer. */
    EC_DEVICE_NOT_MATCH = -20004,
    /** Failed to bind device. */
    EC_BIND_DEVICE_FAILED = -20005,
    /** Instance count is over limit. */
    EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
    /** Trial License */
    EC_TRIAL_LICENSE = -20010,
    /** The license is not valid for current version */
    EC_LICENSE_VERSION_NOT_MATCH = -20011,
    /**Online license validation failed due to network issues. Using cached license information for validation*/
    EC_LICENSE_CACHE_USED = -20012,
    /*License authentication failed: quota exceeded.*/
    EC_LICENSE_AUTH_QUOTA_EXCEEDED = -20013,
    /**License restriction: the number of results has exceeded the allowed limit.*/
    EC_LICENSE_RESULTS_LIMIT_EXCEEDED = -20014,
    /** Failed to reach License Server. */
    EC_FAILED_TO_REACH_DLS = -20200,
    /** -30000~-39999: DBR error code. */
    /** The barcode format is invalid. */
    EC_BARCODE_FORMAT_INVALID = -30009,
    /** The custom module size is invalid. */
    EC_CUSTOM_MODULESIZE_INVALID = -30025,
    /** The frame decoding thread already exists. */
    EC_FRAME_DECODING_THREAD_EXISTS = -30049,
    /** Failed to stop the frame decoding thread. */
    EC_STOP_DECODING_THREAD_FAILED = -30050,
    /**[Barcode Reader] No license found.*/
    EC_BARCODE_READER_LICENSE_NOT_FOUND = -30063,
    /** -40000~-49999: DLR error code */
    /** Character Model file is not found. */
    EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
    /**There is a conflict in the layout of TextLineGroup. */
    EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT = -40101,
    /**There is a conflict in the regex of TextLineGroup. */
    EC_TEXT_LINE_GROUP_REGEX_CONFLICT = -40102,
    /**[Label Recognizer] No license found.*/
    EC_LABEL_RECOGNIZER_LICENSE_NOT_FOUND = -40103,
    /** -50000~-59999: DDN error code. */
    /**No content has been detected. */
    EC_CONTENT_NOT_FOUND = -50056,
    /*The quadrilateral is invalid. */
    EC_QUADRILATERAL_INVALID = -50057,
    /*[Document Normalizer] No license found.*/
    EC_DOCUMENT_NORMALIZER_LICENSE_NOT_FOUND = -50058,
    /** -60000~-69999: DCE error code. */
    /**-60000~-69999: DCE error code*/
    EC_CAMERA_MODULE_NOT_EXIST = -60003;
    EC_CAMERA_ID_NOT_EXIST = -60006;
    EC_NO_SENSOR = -60045;
    /**-70000~-79999: Panorama error code. */
    /** -80000~-89999: Reserved error code. */
    /**-90000~-99999: DCP error code. */
    /** The resource path is not exist. */
    EC_RESOURCE_PATH_NOT_EXIST = -90001,
    /** Failed to load resource. */
    EC_RESOURCE_LOAD_FAILED = -90002,
    /** The code specification is not found. */
    EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
    /** The full code string is empty. */
    EC_FULL_CODE_EMPTY = -90004,
    /** Failed to preprocess the full code string */
    EC_FULL_CODE_PREPROCESS_FAILED = -90005,
    /*[Code Parser] No license found.*/
    EC_CODE_PARSER_LICENSE_NOT_FOUND = -90012
}
```
# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [storekeeper_v1.proto](#storekeeper_v1.proto)
    - [Chunk](#uploader.Chunk)
    - [DownloadableLink](#uploader.DownloadableLink)
    - [Metadata](#uploader.Metadata)
    - [UploadedFileData](#uploader.UploadedFileData)
  
    - [Metadata.ContentType](#uploader.Metadata.ContentType)
  
    - [Uploader](#uploader.Uploader)
  
- [Scalar Value Types](#scalar-value-types)



<a name="storekeeper_v1.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## storekeeper_v1.proto
This file has messages for describing droplez-uploader service


<a name="uploader.Chunk"></a>

### Chunk



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| content | [bytes](#bytes) |  |  |
| file_metadata | [Metadata](#uploader.Metadata) |  |  |






<a name="uploader.DownloadableLink"></a>

### DownloadableLink



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| url | [string](#string) |  |  |






<a name="uploader.Metadata"></a>

### Metadata



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| content_type | [Metadata.ContentType](#uploader.Metadata.ContentType) |  |  |
| local_name | [string](#string) |  |  |
| file_size | [int64](#int64) |  |  |
| user_id | [string](#string) |  |  |






<a name="uploader.UploadedFileData"></a>

### UploadedFileData



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| object | [string](#string) |  |  |





 


<a name="uploader.Metadata.ContentType"></a>

### Metadata.ContentType


| Name | Number | Description |
| ---- | ------ | ----------- |
| CONTENT_TYPE_UNSPECIFIED | 0 |  |
| CONTENT_TYPE_ARCHIVE | 1 |  |
| CONTENT_TYPE_PICTURE | 2 |  |
| CONTENT_TYPE_AUDIO | 3 |  |


 

 


<a name="uploader.Uploader"></a>

### Uploader


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| Upload | [Chunk](#uploader.Chunk) stream | [UploadedFileData](#uploader.UploadedFileData) |  |
| GetDownloadableLink | [UploadedFileData](#uploader.UploadedFileData) | [DownloadableLink](#uploader.DownloadableLink) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |


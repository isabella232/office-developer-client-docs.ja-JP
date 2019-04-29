---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439801"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで使用される圧縮形式から、圧縮されていないリッチテキスト形式 (RTF) でテキストストリームを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>パラメーター

 _lp圧縮 sedrtfstream_
  
> 順番メッセージの PR_RTF_COMPRESSED プロパティで開いているストリームへのポインター。 
    
 _ulFlags_
  
> 順番関数のオプションフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> クライアントが、返されるラップされた stream インターフェイスの読み取りまたは書き込みを行うかどうかを指定します。 
    
STORE_UNCOMPRESSED_RTF 
  
> 非圧縮 RTF は、lpな形式のストリームに__ 書き込む必要があります。
    
 _lp非暗号化 sedrtfstream_
  
> 読み上げ**WrapCompressedRTFStream**が圧縮されていない RTF のストリームを返す場所へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI_MODIFY フラグが_ulflags_パラメーターに渡されている場合、 _lp sedrtfstream_パラメーターは、読み取りおよび書き込みのために既に開いている必要があります。 新しい、非圧縮 RTF テキストは、lp、暗号化されていない_sedrtfストリーム_で返される stream インターフェイスに書き込まれる必要があります。 既存のストリームを追加することはできないため、メッセージテキスト全体を記述する必要があります。 
  
_ulflags_パラメーターに0が渡された場合、 _lp圧縮 sedrtfstream_を読み取り専用で開くことができます。 lpout の出力によって返されるストリームインターフェイスからは、メッセージ__ テキスト全体のみを読み取ることができます。 ストリームの途中から検索することはできません。 
  
 **WrapCompressedRTFStream**は、圧縮ストリームのポインターがストリームの先頭に設定されていることを前提としています。 特定の OLE **IStream**メソッドは、返される非圧縮ストリームではサポートされていません。 **IStream:: Clone**、 **istream:: lockregion**、 **istream:: Revert**、 **istream:: Seek**、istream: **: SetSize**、 **istream:: Stat**、および**istream:: UnlockRegion**が含まれています。 ストリーム全体にコピーするためには、読み取り/書き込みループが必要です。 
  
クライアントは新しい RTF を圧縮されていない形式で書き込むので、ストリームに直接書き込むのではなく、 **WrapCompressedRTFStream**を使用する必要があります。 RTF 対応クライアントは、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで STORE_UNCOMPRESSED_RTF フラグを検索し、設定されている場合は**WrapCompressed RTFStream**に渡す必要があります。 
  
## <a name="see-also"></a>関連項目



[RTFSync](rtfsync.md)


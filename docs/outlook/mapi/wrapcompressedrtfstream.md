---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af4c5b0305f8de8b31ca54747db2d3faed68131f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609188"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで使用される圧縮形式から、圧縮されていないリッチ テキスト形式 (RTF)**で** テキスト ストリームを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
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

 _lpCompressedRTFStream_
  
> [in]メッセージの PR_RTF_COMPRESSEDで開いたストリームへのポインター。 
    
 _ulFlags_
  
> [in]関数のオプション フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_MODIFY 
  
> クライアントが、返されるラップされたストリーム インターフェイスの読み取りまたは書き込みを行う場合。 
    
STORE_UNCOMPRESSED_RTF 
  
> 圧縮されていない RTF は  _、lpCompressedRTFStream が指すストリームに書き込む必要があります_
    
 _lpUncompressedRTFStream_
  
> [out] **WrapCompressedRTFStream** が非圧縮 RTF のストリームを返す場所へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

_ulFlags_ パラメーター MAPI_MODIFYフラグが渡される場合 _、lpCompressedRTFStream_ パラメーターは読み取りおよび書き込みのために既に開いている必要があります。 lpUncompressedRTFStream で返されるストリーム インターフェイスに、圧縮されていない新しい RTF テキスト  _を書き込む必要があります_。 既存のストリームを追加できないので、メッセージ テキスト全体を記述する必要があります。 
  
_ulFlags_ パラメーターにゼロが渡された場合 _、lpCompressedRTFStream_ は読み取り専用で開くことができます。 _lpUncompressedRTFStream_ で返されるストリーム インターフェイスからメッセージ テキスト全体のみを読み取ります。 ストリームの中央から検索はできません。 
  
 **WrapCompressedRTFStream** では、圧縮ストリームのポインターがストリームの先頭に設定されている必要があります。 一部 **の OLE IStream** メソッドは、返される非圧縮ストリームではサポートされていません。 **IStream::Clone**、 **IStream::LockRegion**、 **IStream::Revert**、 **IStream::Seek**、 **IStream::SetSize**、 **IStream::Stat**、**および IStream::UnlockRegion** が含まれます。 ストリーム全体にコピーするには、読み取り/書き込みループが必要です。 
  
クライアントは、圧縮されていない形式で新しい RTF を書き込むため、ストリームに直接書き込む代わりに **WrapCompressedRTFStream** を使用する必要があります。 RTF 対応のクライアントは **、PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで STORE_UNCOMPRESSED_RTF フラグを検索し、それが設定されている場合は **WrapCompressed RTFStream** に渡す必要があります。 
  
## <a name="see-also"></a>関連項目



[RTFSync](rtfsync.md)


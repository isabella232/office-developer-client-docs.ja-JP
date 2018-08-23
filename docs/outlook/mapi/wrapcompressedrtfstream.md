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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9025bcebdd5e656070b31cd82e6519166a3e3791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804250"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**適用対象**: Outlook 
  
圧縮されていない形式 (リッチ テキスト) ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティで使用されている圧縮形式からテキストのストリームを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>パラメーター

 _lpCompressedRTFStream_
  
> [in]メッセージの PR_RTF_COMPRESSED プロパティで開かれているストリームへのポインター。 
    
 _ulFlags_
  
> [in]関数のオプション フラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_MODIFY 
  
> かどうか、クライアントでは、読み取りまたは返されたラップされたストリーム インターフェイスを作成する予定です。 
    
STORE_UNCOMPRESSED_RTF 
  
> 非圧縮の rtf 形式は、 _lpCompressedRTFStream_で示されるストリームに書き込む必要があります。
    
 _lpUncompressedRTFStream_
  
> [out]**WrapCompressedRTFStream**が非圧縮の rtf 形式のストリームを返す場所へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

MAPI_MODIFY フラグが渡された場合、 _ulFlags_パラメーターで、 _lpCompressedRTFStream_パラメーター必要があります読み取りおよび書き込み用に開かれています。 Rtf 形式のテキストが圧縮されていない、新しいは、 _lpUncompressedRTFStream_で返されるストリームのインタ フェースに書き込まれる必要があります。 既存のストリームを追加することはできません、ため、メッセージ テキスト全体を書き込む必要があります。 
  
_UlFlags_パラメーターに 0 を渡した場合、 _lpCompressedRTFStream_開くことができます読み取り専用です。 _LpUncompressedRTFStream_で返されるストリームのインタ フェースからのみ、メッセージ テキスト全体を読み取ることができます。 ストリームの中間の開始を検索することはできません。 
  
 **WrapCompressedRTFStream**では、圧縮されたストリームのポインターをストリームの先頭に設定されていると仮定しています。 返された圧縮解除されたストリームでは、特定の OLE **IStream**のメソッドはサポートされていません。 **IStream::Clone**、 **IStream::LockRegion**、 **IStream::Revert**、 **IStream::Seek**、 **IStream::SetSize**、 **IStream::Stat**、および**IStream::UnlockRegion**が含まれます。 ストリーム全体をコピーするために読み取り/書き込みループが必要です。 
  
クライアントが圧縮されていない形式で新しい RTF を書き込むためのストリームに直接書き込むのではなく、 **WrapCompressedRTFStream**を使用してください。 RTF に対応していないクライアントは、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに STORE_UNCOMPRESSED_RTF フラグを検索し、設定されている場合に、 **WrapCompressed RTFStream**に渡すこと必要があります。 
  
## <a name="see-also"></a>関連項目



[RTFSync](rtfsync.md)


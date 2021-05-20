---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430533"
---
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造を使用すると、圧縮リッチ テキスト形式 (RTF) でメッセージの本文を解凍する情報を指定し、必要に応じて本文ストリームをネイティブ形式で返します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>メンバー

 _size_
  
> 構造体のサイズ **RTF_WCSINFO** バイト数で指定します。 
    
 _ulFlags_
  
> これは [、WrapCompressedRTFStreamEx 関数](wrapcompressedrtfstreamex.md) のオプション フラグのビットマスクです。 サポートされているオプション フラグは次のとおりです。 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |これは、クライアントが返されるラップされたストリーム インターフェイスを書き込むかどうかを示します。  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |これは [、WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数の _lpCompressedRTFStream_ ポインターによって指されるストリームに、圧縮解除された RTF を書き込むかどうかを示します。  <br/> |
|MAPI_NATIVE_BODY  <br/> |これは、圧縮解除されたストリームも、ストリームを返す前にネイティブ本文に変換されるかどうかを示します。 このフラグは、このフラグと組 **み合MAPI_MODIFY** できません。  <br/> |
   
 _ulInCodePage_
  
> これは、メッセージのコード ページ値です。 通常、この値は、メッセージの [PidTagInternetCodepage 標準プロパティ](pidtaginternetcodepage-canonical-property.md) から取得されます。 この値は、ulFlags **でMAPI_NATIVE_BODYフラグ** が渡される  _場合にのみ使用されます_。 それ以外の場合、この値は無視されます。
    
 _ulOutCodePage_
  
> これは、必要な、返される圧縮解除ストリームのコード ページ値です。 これが 0 以外の値に設定されている場合 [、WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) 関数はストリームを指定したコード ページに変換します。 これがゼロ値に設定されている場合、MAPI は使用するコード ページを決定します。 この値は、MAPI_NATIVE_BODYフラグ **が**  _ulFlags_ で渡され、本文形式が RTF ではない場合にのみ使用されます。 それ以外の場合、この値は無視されます。
    
## <a name="see-also"></a>関連項目



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


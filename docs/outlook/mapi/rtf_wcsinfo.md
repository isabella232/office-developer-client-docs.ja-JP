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
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造では、メッセージの本文を圧縮リッチテキスト形式 (RTF) で圧縮解除する情報を指定し、必要に応じて本文ストリームをネイティブ形式で返すことができます。
  
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
  
> **RTF_WCSINFO**構造体のサイズ (バイト数)。 
    
 _ulFlags_
  
> これは、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数のオプションフラグのビットマスクです。 サポートされているオプションフラグは次のとおりです。 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |これは、クライアントが、返されるラップされたストリームインターフェイスを書き込むことを意図しているかどうかを示します。  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |これにより、圧縮されていない RTF が、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数の_lp sedrtfstream_ポインターによって示されるストリームに書き込まれるかどうかを示します。  <br/> |
|MAPI_NATIVE_BODY  <br/> |これは、ストリームを返す前に、圧縮解除されたストリームがネイティブな本文にも変換されるかどうかを示します。 このフラグは、 **MAPI_MODIFY**フラグと組み合わせて使用することはできません。  <br/> |
   
 _ulincodepage_
  
> これは、メッセージのコードページの値です。 通常、この値は、メッセージの[PidTagInternetCodepage 標準プロパティ](pidtaginternetcodepage-canonical-property.md)から取得されます。 この値は、 **MAPI_NATIVE_BODY**フラグが_ulflags_で渡された場合にのみ使用されます。 それ以外の場合、この値は無視されます。
    
 _uloutcodepage_
  
> これは、返される圧縮解除ストリームのコードページの値です。 これが0以外の値に設定されている場合、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数はストリームを指定されたコードページに変換します。 この値が0に設定されている場合、MAPI はどのコードページを使用するかを決定します。 この値は、 **MAPI_NATIVE_BODY**フラグが_ulflags_で渡され、本文の形式が RTF ではない場合にのみ使用されます。 それ以外の場合、この値は無視されます。
    
## <a name="see-also"></a>関連項目



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


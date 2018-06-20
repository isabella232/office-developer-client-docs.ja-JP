---
title: について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803806"
---
# <a name="rtfwcsinfo"></a>について

  
  
**適用されます**: Outlook 
  
この構造体を使用すると、圧縮されたリッチ テキスト形式 (RTF) でメッセージの本文を圧縮解除し、必要に応じて、ネイティブ形式で本文のストリームを返すのための情報を指定できます。
  
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
  
> バイト数**について**の構造体のサイズです。 
    
 _ulFlags_
  
> [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数のオプション フラグのビットマスクです。 サポートされているオプションのフラグは次のとおりです。 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |これは、クライアントが返されたラップされたストリーム インターフェイスを作成しようとしたかどうかを示します。  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |これは、圧縮解除された RTF を[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数の_lpCompressedRTFStream_ポインターによりポイントされているストリームに書き込まれることになっているかどうかを示します。  <br/> |
|MAPI_NATIVE_BODY  <br/> |これは、ストリームを返す前に、ネイティブ形式の本文を圧縮解除されたストリームも変換かどうかを示します。 **MAPI_MODIFY**フラグでこのフラグを組み合わせることはできません。  <br/> |
   
 _ulInCodePage_
  
> これは、メッセージのコード ページ値です。 通常、この値は、メッセージの[PidTagInternetCodepage の標準的なプロパティ](pidtaginternetcodepage-canonical-property.md)から取得されます。 _UlFlags_に**MAPI_NATIVE_BODY**フラグが渡された場合、この値はのみ使用されます。 それ以外の場合、この値は無視されます。
    
 _ulOutCodePage_
  
> これは、使用する返された圧縮解除ストリームのコード ページの値です。 これは、0 以外の値に設定されている場合、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数は、ストリームを指定したコード ページに変換します。 値がゼロに設定すると、MAPI は、使用するコード ページを決定します。 _UlFlags_、 **MAPI_NATIVE_BODY**フラグが渡され、本文が RTF でない場合にのみ、この値が使用されます。 それ以外の場合、この値は無視されます。
    
## <a name="see-also"></a>関連項目



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


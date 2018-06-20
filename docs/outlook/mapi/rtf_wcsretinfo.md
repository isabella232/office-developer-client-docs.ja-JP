---
title: この
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803788"
---
# <a name="rtfwcsretinfo"></a>この

**適用されます**: Outlook 
  
この構造体は、ネイティブ形式の圧縮されたリッチ テキスト形式 (RTF) でカプセル化されたメッセージの本文を圧縮解除から返されるストリームに関する情報を提供します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>メンバー

_size_
  
> バイト数で**この**構造体のサイズです。 
    
_ulStreamFlags_
  
> これは、ネイティブ形式の本文の形式を示す値です。 この値は[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される構造[について](rtf_wcsinfo.md)のパラメーター _ulFlags_に**MAPI_NATIVE_BODY**フラグが渡された場合。 次の値のいずれかを指定できます。 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本体は、rtf 形式の場合、この値はのみ使用されます。  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本文は、テキスト形式の場合、この値はのみ使用されます。  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |_UlFlags_に**MAPI_NATIVE_BODY**フラグが含まれていて、本体は、ハイパー テキスト マークアップ言語 (HTML) 形式の場合、この値はのみ使用されます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


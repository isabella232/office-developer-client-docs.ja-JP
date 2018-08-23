---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564963"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**適用されます**: Outlook 2013 |Outlook 2016 
  
この構造体は、ネイティブ形式の圧縮されたリッチ テキスト形式 (RTF) でカプセル化されたメッセージの本文を圧縮解除から返されるストリームに関する情報を提供します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Members

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


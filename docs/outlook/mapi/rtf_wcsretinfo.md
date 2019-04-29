---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426171"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造体は、圧縮リッチテキスト形式 (RTF) でカプセル化されたメッセージの本文を解凍することによって返されるネイティブ形式のストリームに関する情報を提供します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>メンバー

_size_
  
> **RTF_WCSRETINFO**構造体のサイズ (バイト数)。 
    
_ulstreamflags_
  
> これは、ネイティブ本文の形式を示す値です。 この値は、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される[RTF_WCSINFO](rtf_wcsinfo.md)構造の_ulflags_パラメーターで**MAPI_NATIVE_BODY**フラグが渡された場合にのみ有効です。 次のいずれかの値を指定できます。 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文が RTF の場合にのみ使用されます。  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文がプレーンテキスト形式の場合にのみ使用されます。  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |この値は、 _ulflags_に**MAPI_NATIVE_BODY**フラグが含まれ、本文がハイパーテキストマークアップ言語 (HTML) 形式である場合にのみ使用されます。  <br/> |
   
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


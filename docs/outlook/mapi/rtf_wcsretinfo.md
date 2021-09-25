---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 65d3758cc0abe8835c43887558cdd9f60aeaca85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609608"
---
# <a name="rtf_wcsretinfo"></a>RTF_WCSRETINFO

**適用対象**: Outlook 2013 | Outlook 2016 
  
この構造体は、圧縮リッチ テキスト形式 (RTF) でカプセル化されたメッセージの本文を圧縮解除して返されるネイティブ形式のストリームに関する情報を提供します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>メンバー

_size_
  
> バイト **数RTF_WCSRETINFO構造体** のサイズです。 
    
_ulStreamFlags_
  
> これは、ネイティブ本文の形式を示す値です。 この値は [、wrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数に渡される **RTF_WCSINFO** 構造体の _ulFlags_ パラメーターに [MAPI_NATIVE_BODY](rtf_wcsinfo.md)フラグが渡された場合にのみ有効です。 これには、次のいずれかの値を指定できます。 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |この値は _、ulFlags_ にパラメーターフラグが含MAPI_NATIVE_BODY、本文が RTF の場合にのみ使用されます。  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |この値は _、ulFlags_ に MAPI_NATIVE_BODYフラグが含まれる場合にのみ使用され、本文はプレーン テキスト形式です。  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |この値は _、ulFlags_ に MAPI_NATIVE_BODYフラグが含まれる場合にのみ使用され、本文はハイパーテキスト マークアップ言語 (HTML) 形式です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)


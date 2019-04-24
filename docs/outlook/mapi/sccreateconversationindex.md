---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351325"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージスレッドのメッセージが属する場所を示します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>パラメーター

 _cbparent_
  
> 順番親の会話インデックスのバイト数。
    
 _lpbparent_
  
> 順番親スレッドのインデックス内のバイトへのポインター。 _cbparent_が0の場合、これは NULL になることがあります。 
    
 _lpcbIndex_
  
> 読み上げ呼び出しによって返される新しい会話インデックス内のバイト数へのポインター。 
    
 _lppbindex_
  
> 読み上げ呼び出しによって返される新しい会話インデックスへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    


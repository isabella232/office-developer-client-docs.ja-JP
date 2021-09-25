---
title: メッセージのアイコンの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2016332f5347aeda46d65b03e87cc69f9f359867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614200"
---
# <a name="finding-the-icon-for-a-message"></a>メッセージのアイコンの検索

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージに関連付けられているアイコンを見つけるには**
  
1. メッセージの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得します。
    
2. [MAPIOpenFormMgr を呼び](mapiopenformmgr.md)出して **IMAPIFormMgr インターフェイス ポインターを** 取得します。 pSession パラメーター **で IMAPISession** ポインター  _を渡_ します。 
    
3. [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出して **、IMAPIFormInfo** インターフェイス ポインターを取得します。 
    
4. **IMAPIFormInfo** ポインターを使用して [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出し **、PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティまたは PR_MINI_ICON ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティ **を** 取得します。 
    


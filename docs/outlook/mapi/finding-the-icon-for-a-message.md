---
title: メッセージのアイコンの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409154"
---
# <a name="finding-the-icon-for-a-message"></a>メッセージのアイコンの検索

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージに関連付けられているアイコンを見つけるには**
  
1. メッセージの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得します。
    
2. [MAPIOpenFormMgr を呼び](mapiopenformmgr.md)出して **IMAPIFormMgr インターフェイス ポインターを** 取得します。 pSession パラメーター **で IMAPISession** ポインター  _を渡_ します。 
    
3. [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出して **、IMAPIFormInfo** インターフェイス ポインターを取得します。 
    
4. **IMAPIFormInfo** ポインターを使用して [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出し **、PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティまたは PR_MINI_ICON ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティ **を** 取得します。 
    


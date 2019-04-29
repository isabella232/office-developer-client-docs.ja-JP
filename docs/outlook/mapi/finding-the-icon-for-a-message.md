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
  
 **メッセージに関連付けられているアイコンを検索するには**
  
1. メッセージの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、その**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得します。
    
2. [MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出して、 **imapiformmgr**インターフェイスポインターを取得します。 **imapisession**ポインターを_psession_パラメーターに渡します。 
    
3. [imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出して、 **imapiformmgr**インターフェイスポインターを取得します。 
    
4. **imapiforminfo**ポインターを使用して[、imapiprop:: GetProps](imapiprop-getprops.md)を呼び出し、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティと**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティを取得します。 
    


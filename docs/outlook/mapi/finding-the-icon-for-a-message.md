---
title: メッセージのアイコンの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567812"
---
# <a name="finding-the-icon-for-a-message"></a>メッセージのアイコンの検索

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **メッセージに関連付けられているアイコンを検索するには**
  
1. その**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得するために、メッセージの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。
    
2. **IMAPIFormMgr**インターフェイス ポインターを取得するために[MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出します。 _PSession_パラメーターで、 **IMAPISession**ポインターを渡します。 
    
3. **IMAPIFormInfo**インターフェイス ポインターを取得するために[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出します。 
    
4. **IMAPIFormInfo**ポインターを使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すし、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) や**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティを取得します。 
    


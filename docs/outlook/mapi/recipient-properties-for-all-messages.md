---
title: すべてのメッセージの受信者プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439717"
---
# <a name="recipient-properties-for-all-messages"></a>すべてのメッセージの受信者プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、次のプロパティはすべてのメッセージの受信者に表示されます。 **PR_EMAIL_ADDRESS**および**PR_SEARCH_KEY**は省略可能です。その他のすべてのプロパティが必要です。 
  
**表のタイトル**

|**プロパティ**|**説明**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |メッセージングユーザーの電子メールアドレスの種類 (SMTP など) を格納します。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |指定した MAPI オブジェクトの表示名を格納します。  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |表の特定の行にアイコンを関連付けるために使用される値を格納します。  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |メッセージングユーザーの電子メールアドレスが含まれています。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |特定の mapi オブジェクトのプロパティを開いて編集するために使用する mapi エントリ識別子を含みます。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |オブジェクトの種類を格納します。  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |検索の相関オブジェクトを識別する2つの比較可能なキーが含まれています。  <br/> |
   


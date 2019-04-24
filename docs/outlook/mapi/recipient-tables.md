---
title: 受信者テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328421"
---
# <a name="recipient-tables"></a>受信者テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
recipient テーブルには、メッセージのすべての受信者に関する情報が含まれています。 メッセージストアプロバイダーは受信者テーブルを実装し、クライアントアプリケーションはそれらを使用します。 クライアントは、 [IMessage:: get table](imessage-getrecipienttable.md)メソッドを呼び出して、またはメッセージストアプロバイダーが[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドに対してサポートしている場合に、受信者テーブルにアクセスします。 クライアントは、プロパティタグおよび IID_IMAPITable のインターフェイス識別子に対して**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) を指定することによって、 **openproperty**を使用して受信者テーブルにアクセスします。 受信者テーブルへの変更は、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出すことで行うことができます。 
  
受信者テーブルは、メッセージが送信されたかどうかに応じて異なる列セットを持ちます。 次のプロパティを使用して、受信者テーブルで必要な列セットを作成します。
  
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md))
    
オプションのプロパティは次のとおりです。
  
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS**([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
送信されたメッセージには、必要な列セットにこれらの追加プロパティが含まれている必要があります。
  
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
プロバイダーの実装によっては、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) や[ENTRYID](entryid.md)などの追加の列がテーブルに含まれることがあります。
  
プロバイダーの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで設定されている STORE_SUBMIT_OK ビットによって示されるように、メッセージ転送をサポートするメッセージストアプロバイダーは、特定のセットののサポートを提供する必要があります。受信者テーブルの実装での制限。 **and**、 **OR**、exist、およびプロパティの制限は、受信者テーブルのユーザーが使用できるようにする制限の種類の中にあります。 プロパティ制限で同等および等しくない演算子のみをサポートする必要があります。 これらの制限は、次のプロパティで機能する必要があります。
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)


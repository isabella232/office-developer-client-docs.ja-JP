---
title: アドレス帳のエントリを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803733"
---
# <a name="removing-address-book-entries"></a>アドレス帳のエントリを削除します。
  
**適用されます**: Outlook 
  
1 つまたは複数の受信者を削除するのには、コンテナーの[IABContainer::DeleteEntries](iabcontainer-deleteentries.md)メソッドと呼びます。 **DeleteEntries**には 2 つのパラメーター: 削除する受信者を表すエントリ id と予約済みのフラグの値の配列。 コンテナーのコンテンツ テーブルに影響を受ける受信者を削除します。受信者を削除するには、ほかのコンテナーに受信者を表す内容のテーブルの行を削除しなければなりません。 行がテーブルから削除された、ときに、コンテナーは、各登録済みのクライアントにテーブルの通知を発行する必要があります。 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>IABContainer::DeleteEntries を実装するには
  
1. コンテナーからのエントリの識別子によって表される各受信者を削除します。
    
2. コンテナーの内容のテーブルが開いている場合。
    
   - **UlTableEvent**メンバーが TABLE_ROW_DELETED に設定内容が削除されたテーブルの行ごとに登録されているクライアントに_fnevTableModified_の通知を送信します。 プロバイダーは、通知ユーティリティを使用する場合は、これらの通知を送信するのには[IMAPISupport::Notify](imapisupport-notify.md)を呼び出します。 
    
   - プロバイダーは、オブジェクトの通知をサポートする場合も、 _fnevObjectDeleted_通知を送信します。 
    


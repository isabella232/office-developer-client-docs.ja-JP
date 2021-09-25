---
title: アドレス帳エントリの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ea2671ecdafc5a3cc0445a510613a5eab3dac813
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609671"
---
# <a name="removing-address-book-entries"></a>アドレス帳エントリの削除
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) メソッドが呼び出され、1 つ以上の受信者が削除されます。 **DeleteEntries には** 、削除する受信者を表すエントリ識別子の配列と予約済みのフラグ値の 2 つのパラメーターがあります。 受信者を削除すると、コンテナーのコンテンツ テーブルに影響します。コンテナーは、受信者の削除に加えて、受信者を表す目次行を削除する必要があります。 行がテーブルから削除されると、コンテナーは登録されている各クライアントにテーブル通知を発行する必要があります。 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>IABContainer::D eleteEntries を実装するには
  
1. エントリ識別子によって表される各受信者をコンテナーから削除します。
    
2. コンテナーのコンテンツ テーブルが開いている場合:
    
   - 削除されたコンテンツテーブル行ごとに **、ulTableEvent** メンバーが登録TABLE_ROW_DELETEDに設定された _fnevTableModified_ 通知を送信します。 プロバイダーが通知ユーティリティを使用している場合は [、IMAPISupport::Notify](imapisupport-notify.md) を呼び出して、これらの通知を送信します。 
    
   - プロバイダーがオブジェクト通知をサポートしている場合は  _、fnevObjectDeleted 通知も送信_ します。 
    


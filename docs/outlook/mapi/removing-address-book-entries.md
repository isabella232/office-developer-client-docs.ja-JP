---
title: アドレス帳エントリの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425261"
---
# <a name="removing-address-book-entries"></a>アドレス帳エントリの削除
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの[IABContainer::D eleteentries](iabcontainer-deleteentries.md)メソッドを呼び出して、1人または複数の受信者を削除します。 **deleteentries**には、削除する受信者と予約済みのフラグ値を表すエントリ識別子の配列という2つのパラメーターがあります。 受信者の削除は、コンテナーの contents テーブルに影響します。受信者を削除するだけでなく、コンテナーは、受信者を表すコンテンツテーブルの行を削除する必要があります。 行がテーブルから削除されている場合、コンテナーは登録された各クライアントに対してテーブル通知を発行する必要があります。 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>IABContainer を実装するには::D eleteentries
  
1. エントリ id で表される各受信者をコンテナーから削除します。
    
2. コンテナーの contents テーブルが開いている場合は、次のようになります。
    
   - **ultableevent**メンバーを TABLE_ROW_DELETED に設定して、削除された各目次の表の行について、登録済みのクライアントに_fnevTableModified_通知を送信します。 プロバイダーが通知ユーティリティを使用している場合は、次のような通知を送信するように、 [imapisupport:: Notify](imapisupport-notify.md)を呼び出します。 
    
   - プロバイダーがオブジェクト通知をサポートしている場合は、 _fnevObjectDeleted_通知も送信します。 
    


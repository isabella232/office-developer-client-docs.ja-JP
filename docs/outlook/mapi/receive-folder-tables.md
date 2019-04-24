---
title: 受信フォルダーの表
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328477"
---
# <a name="receive-folder-tables"></a>受信フォルダーの表

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信フォルダーの表には、メッセージストアの受信フォルダーとして指定されたすべてのフォルダーに関する情報が含まれています。 受信フォルダーは、特定のメッセージクラスの受信メッセージが配置されるフォルダーです。 メッセージストアプロバイダーは、受信フォルダーテーブルを実装し、クライアントアプリケーションは[IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)メソッドを呼び出して使用します。 
  
次のプロパティは、受信フォルダーテーブルで必要な列セットを作成します。
  
 **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)


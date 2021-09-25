---
title: メッセージ サービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97952952e48542d6d997285de6847791eefebb49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571970"
---
# <a name="configuring-a-message-service"></a>メッセージ サービスの構成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージ サービス内のすべてのサービス プロバイダーを構成するには**
  
- [IMsgServiceAdmin::ConfigureMsgService を呼び出します](imsgserviceadmin-configuremsgservice.md)。 構成に必要なすべてのデータをプログラムで使用できる場合は、ユーザー インターフェイスを表示するかどうかを選択できます。 ただし、1 つ以上のプロバイダーの情報の一部が使用できない場合は、SERVICE_UI_ALLOWEDまたはSERVICE_UI_ALWAYSしてください。 必要な構成データが使用できない場合にユーザー インターフェイスを抑制すると、構成されていないメッセージ サービスが発生します。
    
 **メッセージ サービスで 1 つのサービス プロバイダーを構成するには**
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、サービス プロバイダーの状態オブジェクトにアクセスします。 
    
2. [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出して、サービス プロバイダーのプロパティ シートを表示します。 
    
状態オブジェクトの使用の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。
  


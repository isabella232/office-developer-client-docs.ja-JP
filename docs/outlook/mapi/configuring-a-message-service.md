---
title: メッセージ サービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434509"
---
# <a name="configuring-a-message-service"></a>メッセージ サービスの構成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージ サービス内のすべてのサービス プロバイダーを構成するには**
  
- [IMsgServiceAdmin::ConfigureMsgService を呼び出します](imsgserviceadmin-configuremsgservice.md)。 構成に必要なすべてのデータをプログラムで使用できる場合は、ユーザー インターフェイスを表示するかどうかを選択できます。 ただし、1 つ以上のプロバイダーの情報の一部が使用できない場合は、SERVICE_UI_ALLOWEDまたはSERVICE_UI_ALWAYSしてください。 必要な構成データが使用できない場合にユーザー インターフェイスを抑制すると、構成されていないメッセージ サービスが発生します。
    
 **メッセージ サービスで 1 つのサービス プロバイダーを構成するには**
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、サービス プロバイダーの状態オブジェクトにアクセスします。 
    
2. [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出して、サービス プロバイダーのプロパティ シートを表示します。 
    
状態オブジェクトの使用の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。
  


---
title: メッセージ サービスを構成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd87d169cd5131c6e1c8ca45a35dded96a295c57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799795"
---
# <a name="configuring-a-message-service"></a>メッセージ サービスを構成します。

  
  
**適用されます**: Outlook 
  
 **メッセージ サービスですべてのサービス プロバイダーを構成するのには**
  
- [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出します。 すべての構成に必要なデータがある場合プログラムでは、ユーザー インターフェイスを表示するかどうかを選択できます。 ただし、1 つまたは複数のプロバイダーの情報の一部が利用できない場合を確認、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS フラグを設定することです。 必要な構成データは、メッセージが構成されていないサービスの結果を使用できない場合は、ユーザー インターフェイスを抑制します。
    
 **メッセージ サービスで 1 つのサービス プロバイダーを構成するのには**
  
1. サービス プロバイダーの状態のオブジェクトにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. サービス プロバイダーのプロパティ シートを表示するのには[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出します。 
    
ステータス オブジェクトの使い方の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。
  


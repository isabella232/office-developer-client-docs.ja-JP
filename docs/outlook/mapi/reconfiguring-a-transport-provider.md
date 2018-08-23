---
title: 転送プロバイダーの再構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5e7c94b387a5fe9f9682854de4097f6f1bbcd786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565600"
---
# <a name="reconfiguring-a-transport-provider"></a>転送プロバイダーの再構成

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロバイダーのプロパティの一部を変更するのには、トランスポート プロバイダーの状態のオブジェクトを使用できます。 変更可能なプロパティの範囲は、プロバイダーのプロパティ シートとプロパティを定義する方法に含まれているプロパティに依存します。 
  
 **トランスポート プロバイダーを再設定するには**
  
1. ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. ターゲット プロバイダーの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致するプロパティの制限を作成することで再構成するトランスポート プロバイダーの行を探します。 
    
3. 適切な行を取得するために[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。 
    
4. ターゲット トランスポート プロバイダーの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティで、STATUS_SETTINGS_DIALOG と STATUS_VALIDATE_STATE のフラグが設定されていることを確認します。 STATUS_SETTINGS_DIALOG が設定されていない場合トランスポート プロバイダーは、[設定] プロパティ シートを表示されません。 STATUS_VALIDATE_STATE が設定されていない場合は、動的再構成を行うことはできません。
    
5. STATUS_SETTINGS_DIALOG が設定されている場合は、トランスポート プロバイダーのプロパティ シートを表示し、ユーザーが変更できるように[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出します。 
    
6. 再構成とともに、ユーザーが完了した後は、STATUS_VALIDATE_STATE を設定すると、CONFIG_CHANGED を渡す場合に[IMAPIStatus::ValidateState](imapistatus-validatestate.md)を呼び出します。 
    


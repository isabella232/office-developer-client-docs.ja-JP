---
title: トランスポート プロバイダーの再構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408412"
---
# <a name="reconfiguring-a-transport-provider"></a>トランスポート プロバイダーの再構成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーの status オブジェクトを使用して、プロバイダーのプロパティの一部を変更できます。 変更できるプロパティの範囲は、プロバイダーのプロパティ シートに含まれるプロパティと、それらのプロパティの定義方法によって異なります。 
  
 **アクティブ なトランスポート プロバイダーを再構成するには**
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。 
    
2. PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とターゲット プロバイダーの名前を一致するプロパティ制限を作成して、再構成するトランスポート プロバイダーの行を探します。 
    
3. [IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、適切な行を取得します。 
    
4. ターゲット トランスポート プロバイダー STATUS_SETTINGS_DIALOG STATUS_VALIDATE_STATE **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティで、PR_RESOURCE_METHODS フラグとパラメーター フラグが設定されているのを確認します。 このSTATUS_SETTINGS_DIALOG設定されていない場合、トランスポート プロバイダーは構成プロパティ シートを表示されません。 このSTATUS_VALIDATE_STATE設定されていない場合は、動的再構成を実行できません。
    
5. このSTATUS_SETTINGS_DIALOG設定されている場合は [、IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) を呼び出してトランスポート プロバイダーのプロパティ シートを表示し、ユーザーが変更を加えるのを許可します。 
    
6. 再構成が完了したら、設定されている場合は [IMAPIStatus::ValidateState](imapistatus-validatestate.md) を呼び出し、STATUS_VALIDATE_STATEを渡CONFIG_CHANGED。 
    


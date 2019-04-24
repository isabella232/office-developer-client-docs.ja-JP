---
title: トランスポートプロバイダーを再構成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328414"
---
# <a name="reconfiguring-a-transport-provider"></a>トランスポートプロバイダーを再構成する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーの status オブジェクトを使用して、プロバイダーのいくつかのプロパティを変更できます。 変更できるプロパティの範囲は、プロバイダーのプロパティシートに含まれているプロパティと、それらのプロパティがどのように定義されているかによって異なります。 
  
 **アクティブなトランスポートプロバイダを再構成するには**
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。 
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とターゲットプロバイダの名前を一致させるプロパティ制限を作成することによって、再構成するトランスポートプロバイダーの行を探します。 
    
3. 必要な行を取得するには、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出します。 
    
4. STATUS_SETTINGS_DIALOG および STATUS_VALIDATE_STATE フラグがターゲットトランスポートプロバイダーの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティで設定されていることを確認します。 STATUS_SETTINGS_DIALOG が設定されていない場合、トランスポートプロバイダーは構成プロパティシートを表示しません。 STATUS_VALIDATE_STATE が設定されていない場合は、動的再構成を実行できません。
    
5. STATUS_SETTINGS_DIALOG が設定されている場合は、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)を呼び出して、トランスポートプロバイダーのプロパティシートを表示し、ユーザーが変更を行えるようにします。 
    
6. ユーザーが再構成を完了した後、STATUS_VALIDATE_STATE が設定されている場合は、CONFIG_CHANGED を渡して、 [imapistatus:: validatestate](imapistatus-validatestate.md)を呼び出します。 
    


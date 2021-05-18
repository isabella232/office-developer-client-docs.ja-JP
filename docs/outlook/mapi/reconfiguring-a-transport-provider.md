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
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="2e62e-103">トランスポート プロバイダーの再構成</span><span class="sxs-lookup"><span data-stu-id="2e62e-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="2e62e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e62e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e62e-105">トランスポート プロバイダーの status オブジェクトを使用して、プロバイダーのプロパティの一部を変更できます。</span><span class="sxs-lookup"><span data-stu-id="2e62e-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="2e62e-106">変更できるプロパティの範囲は、プロバイダーのプロパティ シートに含まれるプロパティと、それらのプロパティの定義方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2e62e-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="2e62e-107">**アクティブ なトランスポート プロバイダーを再構成するには**</span><span class="sxs-lookup"><span data-stu-id="2e62e-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="2e62e-108">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2e62e-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="2e62e-109">PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とターゲット プロバイダーの名前を一致するプロパティ制限を作成して、再構成するトランスポート プロバイダーの行を探します。</span><span class="sxs-lookup"><span data-stu-id="2e62e-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="2e62e-110">[IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、適切な行を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e62e-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="2e62e-111">ターゲット トランスポート プロバイダー STATUS_SETTINGS_DIALOG STATUS_VALIDATE_STATE **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティで、PR_RESOURCE_METHODS フラグとパラメーター フラグが設定されているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e62e-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="2e62e-112">このSTATUS_SETTINGS_DIALOG設定されていない場合、トランスポート プロバイダーは構成プロパティ シートを表示されません。</span><span class="sxs-lookup"><span data-stu-id="2e62e-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="2e62e-113">このSTATUS_VALIDATE_STATE設定されていない場合は、動的再構成を実行できません。</span><span class="sxs-lookup"><span data-stu-id="2e62e-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="2e62e-114">このSTATUS_SETTINGS_DIALOG設定されている場合は [、IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) を呼び出してトランスポート プロバイダーのプロパティ シートを表示し、ユーザーが変更を加えるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="2e62e-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="2e62e-115">再構成が完了したら、設定されている場合は [IMAPIStatus::ValidateState](imapistatus-validatestate.md) を呼び出し、STATUS_VALIDATE_STATEを渡CONFIG_CHANGED。</span><span class="sxs-lookup"><span data-stu-id="2e62e-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    


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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408412"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="1d1fe-103">トランスポートプロバイダーを再構成する</span><span class="sxs-lookup"><span data-stu-id="1d1fe-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="1d1fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d1fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d1fe-105">トランスポートプロバイダーの status オブジェクトを使用して、プロバイダーのいくつかのプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="1d1fe-106">変更できるプロパティの範囲は、プロバイダーのプロパティシートに含まれているプロパティと、それらのプロパティがどのように定義されているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="1d1fe-107">**アクティブなトランスポートプロバイダを再構成するには**</span><span class="sxs-lookup"><span data-stu-id="1d1fe-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="1d1fe-108">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="1d1fe-109">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とターゲットプロバイダの名前を一致させるプロパティ制限を作成することによって、再構成するトランスポートプロバイダーの行を探します。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="1d1fe-110">必要な行を取得するには、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="1d1fe-111">STATUS_SETTINGS_DIALOG および STATUS_VALIDATE_STATE フラグがターゲットトランスポートプロバイダーの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティで設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="1d1fe-112">STATUS_SETTINGS_DIALOG が設定されていない場合、トランスポートプロバイダーは構成プロパティシートを表示しません。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="1d1fe-113">STATUS_VALIDATE_STATE が設定されていない場合は、動的再構成を実行できません。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="1d1fe-114">STATUS_SETTINGS_DIALOG が設定されている場合は、 [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)を呼び出して、トランスポートプロバイダーのプロパティシートを表示し、ユーザーが変更を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="1d1fe-115">ユーザーが再構成を完了した後、STATUS_VALIDATE_STATE が設定されている場合は、CONFIG_CHANGED を渡して、 [imapistatus:: validatestate](imapistatus-validatestate.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1d1fe-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    


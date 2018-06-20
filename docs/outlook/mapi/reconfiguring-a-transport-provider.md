---
title: トランスポート プロバイダーを再構成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ec5a431d04799e3f19c23dd0437aeac13fbf0968
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803728"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="ea2b3-103">トランスポート プロバイダーを再構成します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="ea2b3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea2b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea2b3-105">プロバイダーのプロパティの一部を変更するのには、トランスポート プロバイダーの状態のオブジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="ea2b3-106">変更可能なプロパティの範囲は、プロバイダーのプロパティ シートとプロパティを定義する方法に含まれているプロパティに依存します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="ea2b3-107">**トランスポート プロバイダーを再設定するには**</span><span class="sxs-lookup"><span data-stu-id="ea2b3-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="ea2b3-108">ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="ea2b3-109">ターゲット プロバイダーの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致するプロパティの制限を作成することで再構成するトランスポート プロバイダーの行を探します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="ea2b3-110">適切な行を取得するために[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="ea2b3-111">ターゲット トランスポート プロバイダーの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティで、STATUS_SETTINGS_DIALOG と STATUS_VALIDATE_STATE のフラグが設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="ea2b3-112">STATUS_SETTINGS_DIALOG が設定されていない場合トランスポート プロバイダーは、[設定] プロパティ シートを表示されません。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="ea2b3-113">STATUS_VALIDATE_STATE が設定されていない場合は、動的再構成を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="ea2b3-114">STATUS_SETTINGS_DIALOG が設定されている場合は、トランスポート プロバイダーのプロパティ シートを表示し、ユーザーが変更できるように[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="ea2b3-115">再構成とともに、ユーザーが完了した後は、STATUS_VALIDATE_STATE を設定すると、CONFIG_CHANGED を渡す場合に[IMAPIStatus::ValidateState](imapistatus-validatestate.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea2b3-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    


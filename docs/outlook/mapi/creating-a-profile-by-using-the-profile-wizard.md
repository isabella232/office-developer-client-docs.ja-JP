---
title: プロファイル ウィザードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799857"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="6ed97-103">プロファイル ウィザードを使用したプロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="6ed97-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="6ed97-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ed97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ed97-105">プロファイル ウィザードは、可能な最も簡単な方法でプロファイルを作成するユーザーを有効にする MAPI 機能です。</span><span class="sxs-lookup"><span data-stu-id="6ed97-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="6ed97-106">プロファイル ウィザードでは、一連のメッセージ サービスを選択し、いくつかの最も重要な構成プロパティの値を入力するように求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ed97-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="6ed97-107">その他の必要なプロパティのほとんどは、プロファイル ウィザードは、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ed97-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="6ed97-108">プロファイル ウィザードを起動するには、 **LaunchWizard**、 [LAUNCHWIZARDENTRY](launchwizardentry.md)のプロトタイプでは関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6ed97-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="6ed97-109">ユーザーは、プロファイル ウィザードをサポートする新しいプロファイルに、メッセージ サービスとサービス ・ プロバイダーだけを追加できます。</span><span class="sxs-lookup"><span data-stu-id="6ed97-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="6ed97-110">各メッセージ サービスでは、プロファイル ウィザードが処理できるよりもを設定するその他のプロパティに必要なために、このアプローチを使用する場合ことが、選択したサービスまたは構成が不完全なのでプロバイダーの 1 つ以上に注意します。</span><span class="sxs-lookup"><span data-stu-id="6ed97-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  


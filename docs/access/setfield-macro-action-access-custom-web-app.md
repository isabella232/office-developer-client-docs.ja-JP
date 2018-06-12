---
title: SetField マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: SetField/フィールドの設定アクションでは、フィールドに値を割り当てることができます。
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798738"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="d106f-103">SetField マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="d106f-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d106f-104">" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="d106f-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d106f-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="d106f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d106f-107">[!メモ] " **SetField** /フィールドの設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d106f-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d106f-108">設定</span><span class="sxs-lookup"><span data-stu-id="d106f-108">Setting</span></span>

<span data-ttu-id="d106f-109">" **SetField** /フィールドの設定" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d106f-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="d106f-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="d106f-110">**Argument name**</span></span>|<span data-ttu-id="d106f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d106f-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d106f-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="d106f-112">**Name**</span></span> <br/> |<span data-ttu-id="d106f-113">フィールドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="d106f-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="d106f-114">**値**</span><span class="sxs-lookup"><span data-stu-id="d106f-114">**Value**</span></span> <br/> |<span data-ttu-id="d106f-115">フィールドに割り当てる値を指定する式。</span><span class="sxs-lookup"><span data-stu-id="d106f-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d106f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d106f-116">Remarks</span></span>

<span data-ttu-id="d106f-117">" **SetField** /フィールドの設定" アクションは、 **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** データ ブロック外または **[EditRecord](editrecord-data-block-access-custom-web-app.md)** データ ブロック外では使用できません。</span><span class="sxs-lookup"><span data-stu-id="d106f-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  


---
title: フォームマネージャーでサポートされていない機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419381"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="544b9-103">フォームマネージャーでサポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="544b9-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="544b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="544b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="544b9-105">次の機能は、パフォーマンス上の理由から、既定のフォームマネージャーではサポートされていませんが、カスタムフォームマネージャーでサポートされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="544b9-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="544b9-106">フォームライブラリ全体でフォームをグループ化または分類できる階層。</span><span class="sxs-lookup"><span data-stu-id="544b9-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="544b9-107">フォームライブラリとは、フォームのフラットファイルデータベースのことです。</span><span class="sxs-lookup"><span data-stu-id="544b9-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="544b9-108">メッセージクラスまたはスーパークラスに対応した、フォームのカテゴリのアクセス制御。</span><span class="sxs-lookup"><span data-stu-id="544b9-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="544b9-109">1つのフォームライブラリで同じフォームの複数の言語バージョンがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="544b9-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="544b9-110">これらは実装上の問題です。</span><span class="sxs-lookup"><span data-stu-id="544b9-110">These are implementation issues.</span></span> <span data-ttu-id="544b9-111">カスタムフォームマネージャーがこれらの機能を実装することはできません。</span><span class="sxs-lookup"><span data-stu-id="544b9-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="544b9-112">MAPI フォームのアーキテクチャでは、同時に実行する複数のフォームマネージャーはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="544b9-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="544b9-113">MAPI は複数のメッセージストアプロバイダー、トランスポートプロバイダー、アドレス帳プロバイダーをサポートしていますが、サポートされているのは1つのフォームマネージャーのみです。</span><span class="sxs-lookup"><span data-stu-id="544b9-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="544b9-114">一度に実行できるフォームマネージャーは1つだけなので、カスタムフォームマネージャーを実装する場合は、必要な既定のフォームマネージャーから任意の機能を再実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="544b9-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="544b9-115">カスタムフォームマネージャーは既定のフォームマネージャーを完全に置換するので、既定のフォームマネージャーの機能は、カスタムフォームマネージャーで複製されていない限り使用できません。</span><span class="sxs-lookup"><span data-stu-id="544b9-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="544b9-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="544b9-116">See also</span></span>



[<span data-ttu-id="544b9-117">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="544b9-117">MAPI Forms</span></span>](mapi-forms.md)


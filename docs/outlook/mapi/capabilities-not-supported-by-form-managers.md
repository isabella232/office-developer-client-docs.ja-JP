---
title: フォーム 管理者がサポートしていない機能
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
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="da9ee-103">フォーム 管理者がサポートしていない機能</span><span class="sxs-lookup"><span data-stu-id="da9ee-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="da9ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da9ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da9ee-105">次の機能は、パフォーマンス上の理由から既定のフォーム マネージャーではサポートされていませんが、カスタム フォーム マネージャーでサポートできます。</span><span class="sxs-lookup"><span data-stu-id="da9ee-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="da9ee-106">フォーム ライブラリ全体でフォームをグループ化または分類できる階層。</span><span class="sxs-lookup"><span data-stu-id="da9ee-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="da9ee-107">フォーム ライブラリは、フォームのフラット ファイル データベースです。</span><span class="sxs-lookup"><span data-stu-id="da9ee-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="da9ee-108">メッセージ クラスまたはスーパークラスに対応するフォームのカテゴリのアクセス制御。</span><span class="sxs-lookup"><span data-stu-id="da9ee-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="da9ee-109">1 つのフォーム ライブラリで同じフォームの複数の言語バージョンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="da9ee-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="da9ee-110">これらは実装の問題です。</span><span class="sxs-lookup"><span data-stu-id="da9ee-110">These are implementation issues.</span></span> <span data-ttu-id="da9ee-111">カスタム フォーム マネージャーがこれらの機能を実装するのを防ぐものは何もありません。</span><span class="sxs-lookup"><span data-stu-id="da9ee-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="da9ee-112">MAPI フォーム アーキテクチャでは、同時に実行される複数のフォーム マネージャーはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="da9ee-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="da9ee-113">MAPI は複数の同時メッセージ ストア プロバイダー、トランスポート プロバイダー、アドレス帳プロバイダーをサポートしますが、サポートされるフォーム マネージャーは 1 人のみです。</span><span class="sxs-lookup"><span data-stu-id="da9ee-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="da9ee-114">一度に実行できるのは 1 つのフォーム マネージャーだけなので、カスタム フォーム マネージャーを実装する場合は、必要な既定のフォーム マネージャーから任意の機能を再実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da9ee-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="da9ee-115">カスタム フォーム マネージャーは既定のフォーム マネージャーを完全に置き換えるので、カスタム フォーム マネージャーで重複しない限り、既定のフォーム マネージャーの機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="da9ee-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da9ee-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="da9ee-116">See also</span></span>



[<span data-ttu-id="da9ee-117">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="da9ee-117">MAPI Forms</span></span>](mapi-forms.md)


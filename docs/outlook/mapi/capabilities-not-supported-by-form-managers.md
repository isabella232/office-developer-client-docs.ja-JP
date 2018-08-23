---
title: フォーム マネージャーでサポートされていない機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799748"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="5c4ca-103">フォーム マネージャーでサポートされていない機能</span><span class="sxs-lookup"><span data-stu-id="5c4ca-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="5c4ca-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c4ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c4ca-105">次の機能は、パフォーマンス上の理由から、既定のフォーム マネージャーでサポートされていないが、カスタム フォーム マネージャーをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="5c4ca-106">フォームをグループ化またはフォーム ライブラリ内の分類を可能にする階層です。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="5c4ca-107">フォーム ライブラリは、フォームのフラット ファイル データベースです。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="5c4ca-108">メッセージ クラスまたはスーパークラスに対応する、フォームのカテゴリのアクセス制御です。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="5c4ca-109">1 つのフォーム ライブラリで同じフォームの複数の言語バージョンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="5c4ca-110">これらは、実装の問題です。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-110">These are implementation issues.</span></span> <span data-ttu-id="5c4ca-111">カスタム フォーム マネージャーがこれらの機能を実装することを防止するものがありません。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="5c4ca-112">MAPI フォーム アーキテクチャでは、同時に実行する複数のフォーム マネージャーをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="5c4ca-113">MAPI には、複数の同時のメッセージ ストア プロバイダー、トランスポート プロバイダー、およびアドレス帳プロバイダーがサポートしていれば、1 つのフォーム マネージャーだけはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="5c4ca-114">カスタム フォーム マネージャーを実装する場合にのみ 1 つのフォーム マネージャーを 1 度には、実行可能性がありますのでする必要がある既定のフォーム マネージャーからのすべての機能を再実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="5c4ca-115">ユーザー設定のフォーム マネージャーは、全体的に既定のフォーム マネージャーを置き換えるはため、既定のフォーム マネージャーの機能ことは利用可能なユーザー設定フォームは、マネージャーで重複する場合を除き、します。</span><span class="sxs-lookup"><span data-stu-id="5c4ca-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c4ca-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c4ca-116">See also</span></span>



[<span data-ttu-id="5c4ca-117">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="5c4ca-117">MAPI Forms</span></span>](mapi-forms.md)


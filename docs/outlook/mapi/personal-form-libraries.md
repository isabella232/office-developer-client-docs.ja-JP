---
title: 個人用フォームライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348448"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="ac63f-103">個人用フォームライブラリ</span><span class="sxs-lookup"><span data-stu-id="ac63f-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="ac63f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac63f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac63f-105">その名前が示すように、個人用フォームライブラリには特定のユーザーにとって有用なフォームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac63f-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="ac63f-106">ユーザーの個人用フォームライブラリは、ユーザーのプロファイルで識別される既定のメッセージストアに関連付けられているフォームライブラリです。ワークステーションにインストールされている各プロファイルは、個別の既定のストアを使用します。したがって、個別の個人用フォームライブラリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="ac63f-107">個人用フォームライブラリには、他のフォームに加えて、他のフォームライブラリにも含まれているフォームのコピーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="ac63f-108">個人用フォームライブラリは、サーバー上に存在するか、またはユーザーのワークステーション上でローカルにあるかにかかわらず、ユーザーの既定のメッセージストアにあるルートフォルダーの関連付けられたコンテンツテーブルに実装されます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="ac63f-109">ユーザーの既定のメッセージストアがユーザーのワークステーションに格納されている場合、個人用フォームライブラリでは、アプリケーションがネットワーク上ではなく、ローカルでフォームにアクセスできるようにすることで、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="ac63f-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="ac63f-110">また、オフラインで作業しているユーザーがフォームを使用できるようにすることもできます。これは、ユーザーがネットワークにアクセスすることなく、ポータブルコンピューター上でフォームを取得しようとするときに発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ac63f-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="ac63f-111">個人用フォームライブラリエントリのプロパティと基になる実装には、ローカルエントリを同期する必要があるマスターコンテナーを識別する "Container ID" プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac63f-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="ac63f-112">これは、フォームを含む任意のフォルダーの識別子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ac63f-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="ac63f-113">これは、何らかの種類の組織全体のフォームライブラリをサポートするユーザー設定フォームマネージャーを使用している場合に便利です。フォームマネージャーは、個人用フォームライブラリおよび組織全体のフォームライブラリに保存されているフォームの同期を行います。</span><span class="sxs-lookup"><span data-stu-id="ac63f-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="ac63f-114">これは、フォームマネージャーが読み込まれたときに発生する可能性がありますが、理論的にはいつでも発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ac63f-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac63f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac63f-115">See also</span></span>



[<span data-ttu-id="ac63f-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="ac63f-116">MAPI Forms</span></span>](mapi-forms.md)


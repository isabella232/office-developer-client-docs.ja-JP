---
title: 個人用フォーム ライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420410"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="81c42-103">個人用フォーム ライブラリ</span><span class="sxs-lookup"><span data-stu-id="81c42-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="81c42-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81c42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81c42-105">その名前が示すように、個人用フォーム ライブラリには、特定のユーザーが関心を持つフォームが含まれている。</span><span class="sxs-lookup"><span data-stu-id="81c42-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="81c42-106">ユーザーの個人用フォーム ライブラリは、ユーザーのプロファイルで識別される既定のメッセージ ストアに関連付けられたフォーム ライブラリです。ワークステーションにインストールされている各プロファイルでは、個別の既定のストアを使用できます。したがって、個別の個人用フォーム ライブラリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="81c42-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="81c42-107">個人用フォーム ライブラリには、他のフォームに加えて他のフォーム ライブラリにも含まれるフォームのコピーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="81c42-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="81c42-108">個人用フォーム ライブラリは、ユーザーの既定のメッセージ ストア内のルート フォルダーの関連コンテンツ テーブルに実装されます。サーバー上に存在するか、ユーザーのワークステーション上にローカルに存在するかは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="81c42-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="81c42-109">ユーザーの既定のメッセージ ストアがユーザーのワークステーションに保存されている場合、個人用フォーム ライブラリは、アプリケーションがネットワーク上ではなくローカルでフォームにアクセスできる機能によって、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="81c42-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="81c42-110">また、ユーザーがオフラインで作業しているユーザーがフォームを使用できるようになります。これは、ユーザーがポータブル コンピューターでフォームを持ち、ネットワークにアクセスできない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81c42-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="81c42-111">個人用フォーム ライブラリ エントリのプロパティと基になる実装には、ローカル エントリを同期する必要があるマスター コンテナーを識別する "コンテナー ID" プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81c42-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="81c42-112">フォームを含む任意のフォルダーの識別子を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81c42-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="81c42-113">これは、組織全体のフォーム ライブラリのいくつかの種類をサポートするカスタム フォーム マネージャーを使用している場合に便利です。フォーム マネージャーは、個人用フォーム ライブラリと組織全体のフォーム ライブラリに格納されているフォームの同期を行います。</span><span class="sxs-lookup"><span data-stu-id="81c42-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="81c42-114">これは、おそらくフォーム マネージャーが読み込まれたときに発生しますが、理論的にはいつでも発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81c42-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81c42-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="81c42-115">See also</span></span>



[<span data-ttu-id="81c42-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="81c42-116">MAPI Forms</span></span>](mapi-forms.md)


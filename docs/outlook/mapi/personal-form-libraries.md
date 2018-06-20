---
title: 個人用フォーム ライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801720"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="fd6d2-103">個人用フォーム ライブラリ</span><span class="sxs-lookup"><span data-stu-id="fd6d2-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="fd6d2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd6d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd6d2-105">その名前が示すように、個人用フォーム ライブラリは、特定のユーザーを対象のフォームを含みます。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="fd6d2-106">ユーザーの個人用フォーム ライブラリは、ユーザーのプロファイルで指定された既定のメッセージ ストアに関連付けられているフォーム ライブラリです。ワークステーションにインストールされている各プロファイルには、別の既定のストアでは、およびそのため、別の個人用フォーム ライブラリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="fd6d2-107">個人用フォーム ライブラリには、他のフォームの他には、他のフォーム ライブラリにも含まれているフォームのコピーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="fd6d2-108">個人用フォーム ライブラリがユーザーの既定のメッセージ ストア内のルート フォルダーの内容が関連付けられているテーブルで実装されている、サーバー上またはユーザーのワークステーションにローカルに保存されているかどうか重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="fd6d2-109">ユーザーの既定のメッセージ ストアは、ユーザーのワークステーションに格納されているが、個人用フォーム ライブラリは、ネットワーク経由でローカルの代わりにフォームにアクセスするアプリケーションを有効にするとパフォーマンスの向上を提供します。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="fd6d2-110">また、フォーム利用可能なネットワークにアクセスすることがなく、ユーザーがポータブル コンピューター上でフォームを実行するときに発生する可能性があるユーザーがオフラインで作業します。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="fd6d2-111">プロパティと個人用フォーム ライブラリの項目の基になる実装とローカル エントリを同期する必要がありますマスター コンテナーを識別するためのコンテナー ID プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="fd6d2-112">フォームが含まれている任意のフォルダーの識別子を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="fd6d2-113">組織用フォーム ライブラリのいくつかの並べ替えをサポートするカスタム フォーム マネージャーを使用している場合に便利です。フォーム マネージャーは、個人用フォーム ライブラリ、組織全体のフォーム ライブラリに格納されているフォームを同期する際の注意。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="fd6d2-114">フォーム マネージャーが読み込まれているが、いつでも発生する可能性があります理論的にはこれが可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd6d2-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd6d2-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd6d2-115">See also</span></span>



[<span data-ttu-id="fd6d2-116">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="fd6d2-116">MAPI Forms</span></span>](mapi-forms.md)


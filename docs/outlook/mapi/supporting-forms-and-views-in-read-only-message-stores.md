---
title: �ǂݎ���p�̃��b�Z�[�W �X�g�A�ł̃t�H�[���ƃr���[�̃T�|�[�g
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1ef9b85fd8dad980f92f5e06a4b54daf146fbcec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804044"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="49b6a-103">�ǂݎ���p�̃��b�Z�[�W �X�g�A�ł̃t�H�[���ƃr���[�̃T�|�[�g</span><span class="sxs-lookup"><span data-stu-id="49b6a-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="49b6a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49b6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49b6a-105">メッセージ ストア プロバイダーは、基になるストレージ機構に読み取り専用のアクセス許可を許可している場合クライアント アプリケーションと MAPI フォーム マネージャーができないことを行います。</span><span class="sxs-lookup"><span data-stu-id="49b6a-105">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things.</span></span> <span data-ttu-id="49b6a-106">具体的には、クライアントを追加またはユーザー設定のビューを変更することはできませんし、MAPI フォームのマネージャーがストアのフォルダーの内容が関連付けられているテーブルにフォームをインストールすることができません。</span><span class="sxs-lookup"><span data-stu-id="49b6a-106">Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="49b6a-107">多く読み取り専用のメッセージ ストアは、問題ができない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="49b6a-107">For many read-only message stores, that may not be a problem.</span></span> <span data-ttu-id="49b6a-108">場合は、メッセージ ストア プロバイダーはすべての関連する内容のテーブルをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="49b6a-108">If that is the case, the message store provider does not need to support associated contents tables at all.</span></span> <span data-ttu-id="49b6a-109">ただし場合は、メッセージ ストア プロバイダーが読み取り専用にする必要があり、ビューまたはフォームの定義済みセットもサポートする必要があります、関連付けられている内容のテーブルをサポートするために、必要があります。</span><span class="sxs-lookup"><span data-stu-id="49b6a-109">However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="49b6a-110">最も一般的な戦略のため、これをクライアントと、MAPI フォーム マネージャーには、ビューをインストールできない、またはメッセージにフォームを保存は、メッセージ ストア プロバイダーをハード コーディングするのにメッセージ ・ ストアです。</span><span class="sxs-lookup"><span data-stu-id="49b6a-110">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store.</span></span> <span data-ttu-id="49b6a-111">これは、作成時にメッセージ ・ ストアの存在は内容の関連するテーブルまたはテーブル ビューまたはフォームに含まれていることは、前に、すべてのクライアントまたは MAPI フォーム マネージャーがアクセスを意味します。</span><span class="sxs-lookup"><span data-stu-id="49b6a-111">This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it.</span></span> <span data-ttu-id="49b6a-112">次に、フォームからユーザー設定のビューを取得するのには、関連付けられている内容のテーブルを要求するクライアントまたは MAPI フォームのマネージャーは、フォームを起動するのには、関連付けられている内容のテーブルを要求、ときに、メッセージ ストア プロバイダーはいずれかのデータを提供できます。</span><span class="sxs-lookup"><span data-stu-id="49b6a-112">Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="49b6a-113">内容を関連するテーブルの作成およびメッセージ ストア自体を作成する場合に、この要件が示すように、メッセージ ストア プロバイダーは、そのクライアントと、MAPI フォームに特別なメッセージの形式に関する情報を取得する必要マネージャーは、ビューとフォームの格納に使用します。</span><span class="sxs-lookup"><span data-stu-id="49b6a-113">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms.</span></span> <span data-ttu-id="49b6a-114">なファイル形式とは、クライアントと異なります MAPI フォーム マネージャーを使用しているので、それらの説明をここで提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="49b6a-114">What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49b6a-115">�֘A����</span><span class="sxs-lookup"><span data-stu-id="49b6a-115">See also</span></span>



<span data-ttu-id="49b6a-116">[�ǂݎ���p�̃��b�Z�[�W�̕ۑ�](read-only-message-stores.md)</span><span class="sxs-lookup"><span data-stu-id="49b6a-116">[Read-Only Message Stores](read-only-message-stores.md)</span></span>


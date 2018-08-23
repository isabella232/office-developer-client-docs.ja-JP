---
title: フォルダー フォーム ライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580552"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="b6767-103">フォルダー フォーム ライブラリ</span><span class="sxs-lookup"><span data-stu-id="b6767-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="b6767-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6767-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6767-105">場合によっては、1 つまたは複数のフォームを特定のフォルダーに関連付ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b6767-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="b6767-106">など、組織内の従業員すべてを与えられているの進行状況レポートのフォルダーを作成すると、進行状況レポートを保存するには、その個人メッセージ ストアです。</span><span class="sxs-lookup"><span data-stu-id="b6767-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="b6767-107">進行状況レポートは各ユーザーの進行状況レポートのフォルダーに固有であるため、システム全体のフォーム ライブラリの進行状況の報告書フォームを格納する適切なできない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b6767-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="b6767-108">ただし、各ユーザーの進行状況レポートのフォルダーの内容が関連付けられているテーブルの進行状況レポート フォームのコピーを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="b6767-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="b6767-109">これは、進行状況レポートのフォームを使用して、指定したフォルダーの外部からユーザーを制限します。</span><span class="sxs-lookup"><span data-stu-id="b6767-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="b6767-110">概念的は、メッセージ ・ ストア内のすべてのフォルダーの 1 つのフォルダー フォーム ライブラリにフォームのサーバーがインストールされていない場合でも。</span><span class="sxs-lookup"><span data-stu-id="b6767-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="b6767-111">フォルダー フォーム ライブラリが他のフォーム ライブラリと同じように実装されている、フォルダーの代替部品に関連付けられているコンテンツのテーブルとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="b6767-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="b6767-112">フォルダー フォーム ライブラリが含まれるためフォルダーに、コピー操作では、その親フォルダーと共にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="b6767-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6767-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6767-113">See also</span></span>



[<span data-ttu-id="b6767-114">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="b6767-114">MAPI Forms</span></span>](mapi-forms.md)


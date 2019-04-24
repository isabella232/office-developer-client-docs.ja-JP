---
title: フォルダーフォームライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281558"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="4868c-103">フォルダーフォームライブラリ</span><span class="sxs-lookup"><span data-stu-id="4868c-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="4868c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4868c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4868c-105">場合によっては、1つまたは複数のフォームを特定のフォルダーに関連付けることが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="4868c-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="4868c-106">たとえば、組織内のすべての従業員が、進行状況レポートを作成して保存するために、個人用メッセージストアに進捗レポートフォルダーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4868c-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="4868c-107">進行状況レポートは、各ユーザーの進捗レポートフォルダーに固有のものなので、システム全体のフォームライブラリに進行状況レポートのフォームを保存することは適切ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4868c-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="4868c-108">ただし、進行状況レポートフォームのコピーは、各ユーザーの進行状況レポートフォルダーの関連内容の表に保持できます。</span><span class="sxs-lookup"><span data-stu-id="4868c-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="4868c-109">これにより、ユーザーは指定されたフォルダー以外の進捗レポートフォームを使用できません。</span><span class="sxs-lookup"><span data-stu-id="4868c-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="4868c-110">概念上、フォームサーバーがインストールされていない場合でも、メッセージストア内のすべてのフォルダーに1つのフォルダーフォームライブラリが存在します。</span><span class="sxs-lookup"><span data-stu-id="4868c-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="4868c-111">フォルダーフォームライブラリは、他のフォームライブラリと同様に実装されています。これは、関連付けられたコンテンツテーブルとしてフォルダーの代替部分に格納されます。</span><span class="sxs-lookup"><span data-stu-id="4868c-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="4868c-112">フォルダーにはフォルダーに含まれているため、コピー操作では親フォルダーと一緒にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4868c-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4868c-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="4868c-113">See also</span></span>



[<span data-ttu-id="4868c-114">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="4868c-114">MAPI Forms</span></span>](mapi-forms.md)


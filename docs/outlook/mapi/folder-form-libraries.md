---
title: フォルダー フォーム ライブラリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414285"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="516e4-103">フォルダー フォーム ライブラリ</span><span class="sxs-lookup"><span data-stu-id="516e4-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="516e4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="516e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="516e4-105">場合によっては、1 つ以上のフォームを特定のフォルダーに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="516e4-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="516e4-106">たとえば、組織内の従業員はすべて、進行状況レポートを作成および保存するための個人用メッセージ ストアに進行状況レポート フォルダーを持つ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="516e4-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="516e4-107">進行状況レポートは各ユーザーの進行状況レポート フォルダーに固有なので、進捗レポート フォームをシステム全体のフォーム ライブラリに保存する場合は適切ではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="516e4-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="516e4-108">ただし、進行状況レポート フォームのコピーは、各ユーザーの進行状況レポート フォルダーの関連コンテンツ テーブルに保持できます。</span><span class="sxs-lookup"><span data-stu-id="516e4-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="516e4-109">これにより、指定したフォルダーの外部で進行状況レポート フォームを使用するユーザーが制限されます。</span><span class="sxs-lookup"><span data-stu-id="516e4-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="516e4-110">概念的には、フォーム サーバーがインストールされていない場合でも、メッセージ ストア内のすべてのフォルダーに 1 つのフォルダー フォーム ライブラリがあります。</span><span class="sxs-lookup"><span data-stu-id="516e4-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="516e4-111">フォルダー フォーム ライブラリは、他のフォーム ライブラリと同様に実装され、フォルダーの代替部分に関連コンテンツ テーブルとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="516e4-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="516e4-112">フォルダー フォーム ライブラリはフォルダーに含まれているため、コピー操作で親フォルダーと共にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="516e4-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="516e4-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="516e4-113">See also</span></span>



[<span data-ttu-id="516e4-114">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="516e4-114">MAPI Forms</span></span>](mapi-forms.md)


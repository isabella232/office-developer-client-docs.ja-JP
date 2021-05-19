---
title: MessageBox マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: bdacdafc-728b-4952-b28a-b5c1fe4b4f63
description: MessageBox アクションを使用して、警告や情報メッセージを含むメッセージ ボックスを表示できます。 たとえば、検証マクロで MessageBox アクションを使用できます。コントロールまたはレコードがマクロ内の条件を満たさない場合、メッセージ ボックスにエラー メッセージおよび入力する必要があるデータの種類に関する指示を表示できます。
ms.openlocfilehash: 9f45101fd269ef863e60fd8e69741e5cd7c56ef1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433452"
---
# <a name="messagebox-macro-action-access-custom-web-app"></a><span data-ttu-id="d6821-105">MessageBox マクロ アクション (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="d6821-105">MessageBox Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d6821-p102">" **MessageBox/メッセージボックス** " アクションを使用すると、警告または情報メッセージが含まれるメッセージ ボックスを表示できます。たとえば、" **MessageBox/メッセージボックス** " アクションは入力検査マクロで使用できます。コントロールまたはレコードがマクロの入力検査の条件に適合しない場合は、メッセージ ボックスが表示され、エラー メッセージと入力できるデータの種類に関する説明が示されます。</span><span class="sxs-lookup"><span data-stu-id="d6821-p102">You can use the **MessageBox** action to display a message box containing a warning or an informational message. For example, you can use the **MessageBox** action with validation macros. When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d6821-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="d6821-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d6821-111">設定</span><span class="sxs-lookup"><span data-stu-id="d6821-111">Setting</span></span>

<span data-ttu-id="d6821-112">**MessageBox** アクションには次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="d6821-112">The **MessageBox** action has the following argument.</span></span> 
  
|<span data-ttu-id="d6821-113">**アクションの引数**</span><span class="sxs-lookup"><span data-stu-id="d6821-113">**Action argument**</span></span>|<span data-ttu-id="d6821-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6821-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6821-115">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d6821-115">Message</span></span>  <br/> |<span data-ttu-id="d6821-p104">メッセージ ボックスに表示するテキスト。最大 255 文字または式 (頭に等号記号を付けます) を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6821-p104">The text in the message box. You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span>  <br/> |
   


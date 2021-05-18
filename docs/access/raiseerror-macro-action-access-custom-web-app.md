---
title: RaiseError マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: RaiseError /エラーの生成アクションは、指定されたエラー メッセージが含まれるポップアップ ウィンドウを表示します。
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408244"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="cf086-103">RaiseError マクロ アクション (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="cf086-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="cf086-104">" **RaiseError** /エラーの生成" アクションは、指定されたエラー メッセージが含まれるポップアップ ウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="cf086-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cf086-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="cf086-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cf086-107">"RaiseError/エラーの生成" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf086-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="cf086-108">Setting</span><span class="sxs-lookup"><span data-stu-id="cf086-108">Setting</span></span>

<span data-ttu-id="cf086-109">"**RaiseError**/エラーの生成" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cf086-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="cf086-110">**Arg1 と Arg2 の値**</span><span class="sxs-lookup"><span data-stu-id="cf086-110">**Argument**</span></span>|<span data-ttu-id="cf086-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cf086-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cf086-112">Error Description/エラー説明</span><span class="sxs-lookup"><span data-stu-id="cf086-112">_Error Description_</span></span> <br/> |<span data-ttu-id="cf086-113">エラーを説明する文字列式。</span><span class="sxs-lookup"><span data-stu-id="cf086-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf086-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cf086-114">Remarks</span></span>

<span data-ttu-id="cf086-115">"**RaiseError**/エラーの生成" アクションが呼び出されると、現在のトランザクションのすべての操作がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="cf086-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  


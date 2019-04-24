---
title: DeleteRecord Data マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: DeleteRecord/レコードの削除アクションを使用して、レコードを削除できます。
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282116"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="5dfc0-103">DeleteRecord Data マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="5dfc0-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="5dfc0-104">You can use the **DeleteRecord** action to delete a record.</span><span class="sxs-lookup"><span data-stu-id="5dfc0-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5dfc0-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="5dfc0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5dfc0-107">設定</span><span class="sxs-lookup"><span data-stu-id="5dfc0-107">Setting</span></span>

<span data-ttu-id="5dfc0-108">**DeleteRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5dfc0-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="5dfc0-109">**Arg1 と Arg2 の値**</span><span class="sxs-lookup"><span data-stu-id="5dfc0-109">**Argument**</span></span>|<span data-ttu-id="5dfc0-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="5dfc0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5dfc0-111">**Record Alias/レコードの別名**</span><span class="sxs-lookup"><span data-stu-id="5dfc0-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="5dfc0-112">削除するレコードを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="5dfc0-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="5dfc0-113">*Alias*引数が指定されていない場合は、カレントレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5dfc0-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dfc0-114">解説</span><span class="sxs-lookup"><span data-stu-id="5dfc0-114">Remarks</span></span>

<span data-ttu-id="5dfc0-p103">**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="5dfc0-p103">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block. For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`



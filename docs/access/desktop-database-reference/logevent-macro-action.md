---
title: LogEvent マクロ アクション
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289837"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="9e0a2-102">LogEvent マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="9e0a2-102">LogEvent macro action</span></span>

<span data-ttu-id="9e0a2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e0a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e0a2-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="9e0a2-105">"LogEvent/イベントのログ記録" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="9e0a2-106">Setting</span><span class="sxs-lookup"><span data-stu-id="9e0a2-106">Setting</span></span>

<span data-ttu-id="9e0a2-107">"LogEvent/イベントのログ記録" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e0a2-108">引数</span><span class="sxs-lookup"><span data-stu-id="9e0a2-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="9e0a2-109">必須</span><span class="sxs-lookup"><span data-stu-id="9e0a2-109">Required</span></span></p></th>
<th><p><span data-ttu-id="9e0a2-110">説明</span><span class="sxs-lookup"><span data-stu-id="9e0a2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e0a2-111"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="9e0a2-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="9e0a2-112">いいえ</span><span class="sxs-lookup"><span data-stu-id="9e0a2-112">No</span></span></p></td>
<td><p><span data-ttu-id="9e0a2-p101">記録する条件を説明する文字列式を指定します。説明は 255 文字以内とします。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="9e0a2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="9e0a2-115">Remarks</span></span>

<span data-ttu-id="9e0a2-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="9e0a2-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span><span class="sxs-lookup"><span data-stu-id="9e0a2-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="9e0a2-119">To see the **USysApplicationLog** table, use the following steps:</span><span class="sxs-lookup"><span data-stu-id="9e0a2-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="9e0a2-120">[ **ファイル**] メニューの [ **オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="9e0a2-121">[ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="9e0a2-122">[ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="9e0a2-123">[ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="9e0a2-124">[ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。</span><span class="sxs-lookup"><span data-stu-id="9e0a2-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>


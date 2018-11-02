---
title: LogEvent マクロ アクション
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa036f73dd4c811191c9d5ba83a6d2fc65a54827
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918976"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="048a7-102">LogEvent マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="048a7-102">LogEvent macro action</span></span>


<span data-ttu-id="048a7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="048a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="048a7-104">**LogEvent**アクションは、 **USysApplicationLog**システム ・ テーブルに情報を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="048a7-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="048a7-105"><STRONG>LogEvent</STRONG>アクションは、データ マクロでのみ使用可能。</span><span class="sxs-lookup"><span data-stu-id="048a7-105">The <STRONG>LogEvent</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="048a7-106">設定</span><span class="sxs-lookup"><span data-stu-id="048a7-106">Setting</span></span>

<span data-ttu-id="048a7-107">**LogEvent**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="048a7-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="048a7-108">引数</span><span class="sxs-lookup"><span data-stu-id="048a7-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="048a7-109">必須</span><span class="sxs-lookup"><span data-stu-id="048a7-109">Required</span></span></p></th>
<th><p><span data-ttu-id="048a7-110">説明</span><span class="sxs-lookup"><span data-stu-id="048a7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048a7-111"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="048a7-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="048a7-112">いいえ</span><span class="sxs-lookup"><span data-stu-id="048a7-112">No</span></span></p></td>
<td><p><span data-ttu-id="048a7-p101">記録する条件を説明する文字列式を指定します。説明は 255 文字以内とします。</span><span class="sxs-lookup"><span data-stu-id="048a7-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="048a7-115">備考</span><span class="sxs-lookup"><span data-stu-id="048a7-115">Remarks</span></span>

<span data-ttu-id="048a7-116">**[RaiseError](raiseerror-macro-action.md)** アクションを使用して、エラーをスローする価値がない**USysApplicationLog**システム ・ テーブルに状態情報を書き込むには、 **LogEvent**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="048a7-116">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error.</span></span> <span data-ttu-id="048a7-117">たとえば、特定のフィールドに変更をログに記録または**USysApplicationLog**に書き込む項目を使用して、マクロのデバッグを支援するためできます。</span><span class="sxs-lookup"><span data-stu-id="048a7-117">For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="048a7-118">**LogEvent**アクションを使用して、 **USysApplicationLog**テーブルへの書き込み、**ユーザー**に **[カテゴリ**] 列が自動的に設定します。</span><span class="sxs-lookup"><span data-stu-id="048a7-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="048a7-119">**USysApplicationLog**テーブルを表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="048a7-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="048a7-120">[ **ファイル**] メニューの [ **オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="048a7-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="048a7-121">[ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="048a7-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="048a7-122">[ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="048a7-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="048a7-123">[ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="048a7-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="048a7-124">[ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。</span><span class="sxs-lookup"><span data-stu-id="048a7-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>


---
title: DriverPromptEnum 列挙 (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c20542c89537f16f20c9d3e30cbc14ce115bf4d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479597"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="d40f5-102">DriverPromptEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="d40f5-102">DriverPromptEnum Enumeration (DAO)</span></span>


<span data-ttu-id="d40f5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d40f5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d40f5-104">ユーザーに接続を確立するための確認のメッセージを表示するかどうか、またいつ表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d40f5-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d40f5-105">名前</span><span class="sxs-lookup"><span data-stu-id="d40f5-105">Name</span></span></p></th>
<th><p><span data-ttu-id="d40f5-106">値</span><span class="sxs-lookup"><span data-stu-id="d40f5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d40f5-107">説明</span><span class="sxs-lookup"><span data-stu-id="d40f5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d40f5-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="d40f5-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="d40f5-109">0</span><span class="sxs-lookup"><span data-stu-id="d40f5-109">0</span></span></p></td>
<td><p><span data-ttu-id="d40f5-110">指定された接続文字列に DSN キーワードが含まれている場合、ドライバー マネージャーはその文字列を接続でそのまま使用します。それ以外の場合は、<strong>dbDriverPrompt</strong> が指定されたときと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="d40f5-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d40f5-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="d40f5-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="d40f5-112">3</span><span class="sxs-lookup"><span data-stu-id="d40f5-112">3</span></span></p></td>
<td><p><span data-ttu-id="d40f5-113">(既定値) <strong>dbDriverComplete</strong> が指定されたときと同じように動作します。ただし、ドライバーは接続を完了するために必要ではないすべての情報のためのコントロールを無効にします。</span><span class="sxs-lookup"><span data-stu-id="d40f5-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d40f5-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="d40f5-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="d40f5-115">1</span><span class="sxs-lookup"><span data-stu-id="d40f5-115">1</span></span></p></td>
<td><p><span data-ttu-id="d40f5-p101">ドライバー マネージャーは指定された接続文字列を接続で使用します。十分な情報が指定されていない場合は、トラップ可能なエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="d40f5-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d40f5-118">そのまま使用</span><span class="sxs-lookup"><span data-stu-id="d40f5-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="d40f5-119">2</span><span class="sxs-lookup"><span data-stu-id="d40f5-119">2</span></span></p></td>
<td><p><span data-ttu-id="d40f5-p102">ドライバー マネージャーは [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを表示します。接続の確立に使用される接続文字列は、このダイアログ ボックスを通じてユーザーが選択および完成させたデータ ソース名 (DSN) から構築されます。</span><span class="sxs-lookup"><span data-stu-id="d40f5-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>


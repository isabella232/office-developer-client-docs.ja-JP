---
title: DriverPromptEnum 列挙 (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293666"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="54843-102">DriverPromptEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="54843-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="54843-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="54843-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54843-104">ユーザーに接続を確立するための確認のメッセージを表示するかどうか、またいつ表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54843-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54843-105">名前</span><span class="sxs-lookup"><span data-stu-id="54843-105">Name</span></span></p></th>
<th><p><span data-ttu-id="54843-106">値</span><span class="sxs-lookup"><span data-stu-id="54843-106">Value</span></span></p></th>
<th><p><span data-ttu-id="54843-107">説明</span><span class="sxs-lookup"><span data-stu-id="54843-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54843-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="54843-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="54843-109">.0</span><span class="sxs-lookup"><span data-stu-id="54843-109">0</span></span></p></td>
<td><p><span data-ttu-id="54843-110">指定された接続文字列に DSN キーワードが含まれている場合、ドライバー マネージャーはその文字列を接続でそのまま使用します。それ以外の場合は、<strong>dbDriverPrompt</strong> が指定されたときと同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="54843-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54843-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="54843-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="54843-112">1/3</span><span class="sxs-lookup"><span data-stu-id="54843-112">3</span></span></p></td>
<td><p><span data-ttu-id="54843-113">(既定値) <strong>dbDriverComplete</strong> が指定されたときと同じように動作します。ただし、ドライバーは接続を完了するために必要ではないすべての情報のためのコントロールを無効にします。</span><span class="sxs-lookup"><span data-stu-id="54843-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54843-114">dbdrivernoprompt</span><span class="sxs-lookup"><span data-stu-id="54843-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="54843-115">1-d</span><span class="sxs-lookup"><span data-stu-id="54843-115">1</span></span></p></td>
<td><p><span data-ttu-id="54843-p101">ドライバー マネージャーは指定された接続文字列を接続で使用します。十分な情報が指定されていない場合は、トラップ可能なエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="54843-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54843-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="54843-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="54843-119">pbm-2</span><span class="sxs-lookup"><span data-stu-id="54843-119">2</span></span></p></td>
<td><p><span data-ttu-id="54843-p102">ドライバー マネージャーは [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを表示します。接続の確立に使用される接続文字列は、このダイアログ ボックスを通じてユーザーが選択および完成させたデータ ソース名 (DSN) から構築されます。</span><span class="sxs-lookup"><span data-stu-id="54843-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>


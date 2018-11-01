---
title: Command オブジェクトの概要
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39724156b8644b6d99ffec82bdf79624b6cfaee1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875036"
---
# <a name="command-object-overview"></a><span data-ttu-id="41a26-102">Command オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="41a26-102">Command Object Overview</span></span>


<span data-ttu-id="41a26-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="41a26-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41a26-104">**Command** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="41a26-105">**CommandText** プロパティを使用して、コマンドの実行可能なテキスト (SQL ステートメントやストアド プロシージャなど) を定義できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="41a26-106">**Parameter** オブジェクトと **Parameters** コレクションを使用して、パラメーター付きクエリやストアド プロシージャの引数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="41a26-107">**Execute** メソッドを使用して、コマンドを実行し、必要に応じて **Recordset** オブジェクトを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="41a26-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="41a26-108">**CommandType** プロパティを使用して、コマンドを実行する前にそのコマンドの種類を指定し、パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="41a26-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="41a26-109">**Prepared** プロパティを使用して、コマンドの実行前に、プロバイダーがそのコマンドの準備された (コンパイル済みの) バージョンを保存するかどうかを制御できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="41a26-110">**CommandTimeout** プロパティを使用して、コマンドの実行までプロバイダーが待機する時間を秒数で設定できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="41a26-111">**Command** オブジェクトの **ActiveConnection** プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="41a26-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="41a26-112">**Name** プロパティを設定して、 **Command** オブジェクトを関連付けられている **Connection** オブジェクトのメソッドとして識別できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="41a26-113">**Command** オブジェクトを **Recordset** の **Source** プロパティに渡すことにより、データを取得できます。</span><span class="sxs-lookup"><span data-stu-id="41a26-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>


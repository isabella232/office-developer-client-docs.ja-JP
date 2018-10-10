---
title: CommandTimeout プロパティ (ADO)
TOCTitle: CommandTimeout Property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 58d95f6a3238d09ae10ddb3ba127a9fa68631f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477000"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="24c5f-102">CommandTimeout プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="24c5f-102">CommandTimeout Property (ADO)</span></span>


<span data-ttu-id="24c5f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="24c5f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="24c5f-104">実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="24c5f-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="24c5f-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="24c5f-105">Settings and Return Values</span></span>

<span data-ttu-id="24c5f-p101">コマンドが実行されるまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 30 です。</span><span class="sxs-lookup"><span data-stu-id="24c5f-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute. Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c5f-108">解説</span><span class="sxs-lookup"><span data-stu-id="24c5f-108">Remarks</span></span>

<span data-ttu-id="24c5f-p102">ネットワーク トラフィックやサーバーの過負荷により実行が遅れている **Execute** メソッドの呼び出しを取り消すことができるようにするには、 [Connection](connection-object-ado.md) オブジェクトまたは [Command](command-object-ado.md) オブジェクトの [CommandTimeout](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) プロパティを使用します。コマンドの実行が完了する前に **CommandTimeout** プロパティで設定された時間が経過すると、エラーが発生してコマンドが取り消されます。プロパティを 0 に設定すると、コマンド実行が完了するまで無限に待機します。コードを書き込むプロバイダーとデータ ソースが **CommandTimeout** 機能をサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="24c5f-p102">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method call, due to delays from network traffic or heavy server use. If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command. If you set the property to zero, ADO will wait indefinitely until the execution is complete. Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="24c5f-113">**Connection** オブジェクトの **CommandTimeout** 設定は、同じ **Connection** 上の **Command** オブジェクトの **CommandTimeout** 設定に影響しません。つまり、 **Command** オブジェクトの **CommandTimeout** プロパティは、 **Connection** オブジェクトの **CommandTimeout** の値を継承しません。</span><span class="sxs-lookup"><span data-stu-id="24c5f-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="24c5f-114">**Connection** オブジェクトでは、 **CommandTimeout** プロパティは **Connection** が開かれた後も、読み取り/書き込みが可能です。</span><span class="sxs-lookup"><span data-stu-id="24c5f-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>


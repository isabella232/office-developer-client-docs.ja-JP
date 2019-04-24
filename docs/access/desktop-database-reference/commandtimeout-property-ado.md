---
title: CommandTimeout プロパティ (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296130"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="a1238-102">CommandTimeout プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a1238-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="a1238-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1238-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1238-104">実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="a1238-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a1238-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="a1238-105">Settings and return values</span></span>

<span data-ttu-id="a1238-106">コマンドが実行されるまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a1238-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute.</span></span> <span data-ttu-id="a1238-107">既定値は 30 です。</span><span class="sxs-lookup"><span data-stu-id="a1238-107">Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1238-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a1238-108">Remarks</span></span>

<span data-ttu-id="a1238-p102">ネットワーク トラフィックやサーバーの過負荷により実行が遅れている **Execute** メソッドの呼び出しを取り消すことができるようにするには、 [Connection](connection-object-ado.md) オブジェクトまたは [Command](command-object-ado.md) オブジェクトの [CommandTimeout](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) プロパティを使用します。コマンドの実行が完了する前に **CommandTimeout** プロパティで設定された時間が経過すると、エラーが発生してコマンドが取り消されます。プロパティを 0 に設定すると、コマンド実行が完了するまで無限に待機します。コードを書き込むプロバイダーとデータ ソースが **CommandTimeout** 機能をサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a1238-p102">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use. If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command. If you set the property to zero, ADO will wait indefinitely until the execution is complete. Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="a1238-113">**Connection** オブジェクトの **CommandTimeout** 設定は、同じ **Connection** 上の **Command** オブジェクトの **CommandTimeout** 設定に影響しません。つまり、 **Command** オブジェクトの **CommandTimeout** プロパティは、 **Connection** オブジェクトの **CommandTimeout** の値を継承しません。</span><span class="sxs-lookup"><span data-stu-id="a1238-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="a1238-114">**Connection** オブジェクトでは、 **CommandTimeout** プロパティは **Connection** が開かれた後も、読み取り/書き込みが可能です。</span><span class="sxs-lookup"><span data-stu-id="a1238-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>


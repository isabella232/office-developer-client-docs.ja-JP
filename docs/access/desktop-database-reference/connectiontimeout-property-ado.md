---
title: ConnectionTimeout プロパティ (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295703"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="1ad7f-102">ConnectionTimeout プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ad7f-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="1ad7f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ad7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ad7f-104">接続操作を中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="1ad7f-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1ad7f-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="1ad7f-105">Settings and return values</span></span>

<span data-ttu-id="1ad7f-106">接続が開くまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="1ad7f-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="1ad7f-107">既定値は 15 です。</span><span class="sxs-lookup"><span data-stu-id="1ad7f-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad7f-108">注釈</span><span class="sxs-lookup"><span data-stu-id="1ad7f-108">Remarks</span></span>

<span data-ttu-id="1ad7f-p102">ネットワーク トラフィックやサーバーの過度の使用が原因で接続を開く試みを中止する必要がある場合は、**Connection** オブジェクトで [ConnectionTimeout](connection-object-ado.md) プロパティを使用します。接続が開かれる前に **ConnectionTimeout** プロパティで設定した時間が経過した場合は、エラーが発生して接続の試みが取り消されます。このプロパティを 0 に設定した場合は、ADO は接続が開かれるまで無限に待機します。コードを書き込むプロバイダーが、 **ConnectionTimeout** 機能をサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1ad7f-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="1ad7f-113">**ConnectionTimeout** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="1ad7f-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>


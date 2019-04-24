---
title: marshaloptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289771"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="539a8-102">marshaloptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="539a8-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="539a8-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="539a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="539a8-104">どのレコードがサーバーにマーシャリングされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="539a8-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="539a8-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="539a8-105">Settings And Return Values</span></span>

<span data-ttu-id="539a8-p101">[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。</span><span class="sxs-lookup"><span data-stu-id="539a8-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="539a8-108">注釈</span><span class="sxs-lookup"><span data-stu-id="539a8-108">Remarks</span></span>

<span data-ttu-id="539a8-109">クライアント側の[Recordset](recordset-object-ado.md)を使用する場合、クライアント上で変更されたレコードは、マーシャリングと呼ばれる手法を使用して中間層または web サーバーに書き戻されます。これは、スレッド間でインターフェイスメソッドのパラメーターをパッケージ化して送信するプロセスです。プロセス境界。</span><span class="sxs-lookup"><span data-stu-id="539a8-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="539a8-110">**marshaloptions**プロパティを設定すると、変更されたリモートデータを中央層または web サーバーに戻すためにマーシャリングするときのパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="539a8-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="539a8-111">**リモートデータサービスの使用状況**このプロパティは、クライアント側の**Recordset**でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="539a8-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>


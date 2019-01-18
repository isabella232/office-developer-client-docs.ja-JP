---
title: MarshalOptions プロパティ (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704596"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="0dc55-102">MarshalOptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dc55-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="0dc55-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0dc55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dc55-104">どのレコードがサーバーにマーシャリングされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="0dc55-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0dc55-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="0dc55-105">Settings And Return Values</span></span>

<span data-ttu-id="0dc55-p101">[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。</span><span class="sxs-lookup"><span data-stu-id="0dc55-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc55-108">解説</span><span class="sxs-lookup"><span data-stu-id="0dc55-108">Remarks</span></span>

<span data-ttu-id="0dc55-109">クライアント側の[Recordset](recordset-object-ado.md)を使用すると、クライアント上で変更されたレコードに書き込まれます戻る、中間層またはマーシャ リングをパッケージ化し、スレッド間でインターフェイス メソッドのパラメーターを送信するという手法を使用して web サーバーまたはプロセス境界という考え方です。</span><span class="sxs-lookup"><span data-stu-id="0dc55-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="0dc55-110">**スレッド**を設定すると、リモート データが変更されたが、中間層または web サーバーに更新するためにマーシャ リングするときにパフォーマンスが向上することができます。</span><span class="sxs-lookup"><span data-stu-id="0dc55-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="0dc55-111">**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="0dc55-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>


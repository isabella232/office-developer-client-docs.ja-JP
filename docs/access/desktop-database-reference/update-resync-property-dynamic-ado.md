---
title: Update Resync 動的プロパティ (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308345"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="270ef-102">Update Resync 動的プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="270ef-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="270ef-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="270ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="270ef-104">[UpdateBatch](updatebatch-method-ado.md) メソッドの後に暗黙の [Resync](resync-method-ado.md) メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="270ef-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="270ef-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="270ef-105">Settings and return values</span></span>

<span data-ttu-id="270ef-106">1つまたは複数の[adcprop\_\_UPDATERESYNC 列挙](adcprop-updateresync-enum.md)値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="270ef-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="270ef-107">注釈</span><span class="sxs-lookup"><span data-stu-id="270ef-107">Remarks</span></span>

<span data-ttu-id="270ef-108">adcprop\_UPDATERESYNC\_列挙体の値は、他の値の組み合わせを既に表す adResyncAll を除き、組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="270ef-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="270ef-109">定数 **adResyncConflicts** は、再同期値を基になる値として保存しますが、保留中の変更は上書きしません。</span><span class="sxs-lookup"><span data-stu-id="270ef-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="270ef-110">**Update Resync** は、 [CursorLocation](recordset-object-ado.md) プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="270ef-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>


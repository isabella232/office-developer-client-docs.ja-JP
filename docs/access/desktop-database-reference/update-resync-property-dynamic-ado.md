---
title: Update Resync プロパティ -- 動的 (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477771"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="bd9bf-102">Update Resync プロパティ -- 動的 (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd9bf-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="bd9bf-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd9bf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd9bf-104">[UpdateBatch](updatebatch-method-ado.md) メソッドの後に暗黙の [Resync](resync-method-ado.md) メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd9bf-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bd9bf-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="bd9bf-105">Settings and Return Values</span></span>

<span data-ttu-id="bd9bf-106">いずれかを取得または設定します[ADCPROP\_UPDATERESYNC\_列挙型](adcprop-updateresync-enum.md)の値です。</span><span class="sxs-lookup"><span data-stu-id="bd9bf-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd9bf-107">備考</span><span class="sxs-lookup"><span data-stu-id="bd9bf-107">Remarks</span></span>

<span data-ttu-id="bd9bf-108">ADCPROP の値\_UPDATERESYNC\_既に残りの値の組み合わせを表す adResyncAll を除いて、列挙型を組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="bd9bf-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="bd9bf-109">定数 **adResyncConflicts** は、再同期値を基になる値として保存しますが、保留中の変更は上書きしません。</span><span class="sxs-lookup"><span data-stu-id="bd9bf-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="bd9bf-110">**Update Resync** は、 [CursorLocation](recordset-object-ado.md) プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="bd9bf-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>


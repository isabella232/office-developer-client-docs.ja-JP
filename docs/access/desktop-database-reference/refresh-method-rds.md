---
title: Refresh メソッド (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b52d6a4250f19709dd72dbedd516c9a88c0522c7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926291"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="849c4-102">Refresh メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="849c4-102">Refresh method (RDS)</span></span>


<span data-ttu-id="849c4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="849c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="849c4-104">[Connect](connect-property-rds.md) プロパティで指定されたデータ ソースに再度クエリを実行し、クエリの結果を更新します。</span><span class="sxs-lookup"><span data-stu-id="849c4-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="849c4-105">構文</span><span class="sxs-lookup"><span data-stu-id="849c4-105">Syntax</span></span>

<span data-ttu-id="849c4-106">*DataControl*。更新</span><span class="sxs-lookup"><span data-stu-id="849c4-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="849c4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="849c4-107">Parameters</span></span>

  - <span data-ttu-id="849c4-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="849c4-108">*DataControl*</span></span>

  - <span data-ttu-id="849c4-109">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="849c4-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="849c4-110">解説</span><span class="sxs-lookup"><span data-stu-id="849c4-110">Remarks</span></span>

<span data-ttu-id="849c4-p101">[Refresh](connect-property-rds.md) メソッドを使用する前に、 [Connect](server-property-rds.md) プロパティ、 [Server](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) プロパティ、および **SQL** プロパティを設定する必要があります。 **RDS.DataControl** オブジェクトに関連付けられたフォーム上のすべてのデータ連結コントロールに、レコードの新しいセットが反映されます。既存の [Recordset](recordset-object-ado.md) オブジェクトはすべて解放され、保存されていない変更はすべて破棄されます。 **Refresh** メソッドは、自動的に最初のレコードをカレント レコードに設定します。</span><span class="sxs-lookup"><span data-stu-id="849c4-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="849c4-p102">データを操作するときは、 **Refresh** メソッドを定期的に呼び出すことをお勧めします。データを取得してから、クライアント コンピューター上でしばらくそのままにしておくと、データが古くなる可能性があります。また、他のユーザーが同じレコードを変更し、自分よりも先に変更を適用する場合があるため、そのレコードの変更に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="849c4-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>


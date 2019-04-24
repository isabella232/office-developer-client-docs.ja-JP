---
title: Refresh メソッド (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309300"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="c2595-102">Refresh メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="c2595-102">Refresh method (RDS)</span></span>

<span data-ttu-id="c2595-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2595-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2595-104">[Connect](connect-property-rds.md) プロパティで指定されたデータ ソースに再度クエリを実行し、クエリの結果を更新します。</span><span class="sxs-lookup"><span data-stu-id="c2595-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2595-105">構文</span><span class="sxs-lookup"><span data-stu-id="c2595-105">Syntax</span></span>

<span data-ttu-id="c2595-106">*DataControl*。更新</span><span class="sxs-lookup"><span data-stu-id="c2595-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="c2595-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2595-107">Parameters</span></span>

|<span data-ttu-id="c2595-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2595-108">Parameter</span></span>|<span data-ttu-id="c2595-109">説明</span><span class="sxs-lookup"><span data-stu-id="c2595-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c2595-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c2595-110">*DataControl*</span></span> |<span data-ttu-id="c2595-111">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="c2595-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c2595-112">注釈</span><span class="sxs-lookup"><span data-stu-id="c2595-112">Remarks</span></span>

<span data-ttu-id="c2595-p101">[Refresh](connect-property-rds.md) メソッドを使用する前に、 [Connect](server-property-rds.md) プロパティ、 [Server](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) プロパティ、および **SQL** プロパティを設定する必要があります。 **RDS.DataControl** オブジェクトに関連付けられたフォーム上のすべてのデータ連結コントロールに、レコードの新しいセットが反映されます。既存の [Recordset](recordset-object-ado.md) オブジェクトはすべて解放され、保存されていない変更はすべて破棄されます。 **Refresh** メソッドは、自動的に最初のレコードをカレント レコードに設定します。</span><span class="sxs-lookup"><span data-stu-id="c2595-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="c2595-p102">データを操作するときは、 **Refresh** メソッドを定期的に呼び出すことをお勧めします。データを取得してから、クライアント コンピューター上でしばらくそのままにしておくと、データが古くなる可能性があります。また、他のユーザーが同じレコードを変更し、自分よりも先に変更を適用する場合があるため、そのレコードの変更に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c2595-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>


---
title: Recordset2.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54ec9af0b8fa1948afe568dc57eacf9962283504
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476730"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="c449e-102">Recordset2.Updatable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c449e-102">Recordset2.Updatable Property (DAO)</span></span>


<span data-ttu-id="c449e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c449e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c449e-p101">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c449e-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c449e-106">構文</span><span class="sxs-lookup"><span data-stu-id="c449e-106">Syntax</span></span>

<span data-ttu-id="c449e-107">*式*です。更新可能です</span><span class="sxs-lookup"><span data-stu-id="c449e-107">*expression* .Updatable</span></span>

<span data-ttu-id="c449e-108">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c449e-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c449e-109">備考</span><span class="sxs-lookup"><span data-stu-id="c449e-109">Remarks</span></span>

<span data-ttu-id="c449e-110">スナップショットと前方スクロールのタイプの Recordset オブジェクトは常に**False**を返します。</span><span class="sxs-lookup"><span data-stu-id="c449e-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="c449e-p102">オブジェクトの種類の中には、更新できないフィールドが含まれている場合がよくあります。たとえば、一部のフィールドしか変更できないようなダイナセット タイプの **Recordset** オブジェクトを作成することもできます。これらのフィールドは固定にすることも、自動的に増加するデータを含めることもでき、また更新可能なテーブルと更新できないテーブルを組み合わせたクエリによってダイナセットを得ることもできます。</span><span class="sxs-lookup"><span data-stu-id="c449e-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="c449e-p103">オブジェクトに読み取り専用フィールドしか含まれていない場合、 **Updatable** プロパティの値は **False** となります。1 つ以上のフィールドが更新可能な場合、このプロパティの値は **True** となります。更新可能なフィールドのみ編集できます。新しい値を読み取り専用フィールドに割り当てると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c449e-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="c449e-118">更新可能なオブジェクトには読み取り専用フィールドが含まれていることがあるため、レコードを編集する前に、 **Recordset** オブジェクトの **Fields** コレクションの各フィールドの **DataUpdatable** プロパティを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c449e-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

---
title: Source プロパティ (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308597"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="aec6c-102">Source プロパティ (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="aec6c-102">Source property (ADO Error)</span></span>


<span data-ttu-id="aec6c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="aec6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aec6c-104">エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="aec6c-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="aec6c-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="aec6c-105">Return value</span></span>

<span data-ttu-id="aec6c-106">オブジェクトまたはアプリケーションの名前を示す文字列型 (**String**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="aec6c-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec6c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="aec6c-107">Remarks</span></span>

<span data-ttu-id="aec6c-108">エラーが発生した元のオブジェクトまたはアプリケーションの名前を確認するには、 [error](error-object-ado.md)オブジェクトの**Source**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="aec6c-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="aec6c-109">これは、オブジェクトのクラス名またはプログラム ID である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aec6c-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="aec6c-110">ADO のエラーについては、プロパティの値は \*\*ADODB. \*\*\* (objectname) になります。 *objectname*は、エラーを発生させたオブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="aec6c-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="aec6c-111">ADOX および ADO MD の場合、値はそれぞれ \**adox. \* \* \* objectname*および \**adomd.nethttp \* \* objectname*となります。</span><span class="sxs-lookup"><span data-stu-id="aec6c-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="aec6c-112">**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。</span><span class="sxs-lookup"><span data-stu-id="aec6c-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="aec6c-113">**Error** オブジェクトの **Source** プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="aec6c-113">The **Source** property is read-only for **Error** objects.</span></span>


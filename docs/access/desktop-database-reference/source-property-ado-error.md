---
title: Source プロパティ (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dcc674a570b3d2adf6108316339a86333a82f9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477800"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="58150-102">Source プロパティ (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="58150-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="58150-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="58150-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58150-104">エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="58150-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="58150-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="58150-105">Return Value</span></span>

<span data-ttu-id="58150-106">オブジェクトまたはアプリケーションの名前を示す文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="58150-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="58150-107">解説</span><span class="sxs-lookup"><span data-stu-id="58150-107">Remarks</span></span>

<span data-ttu-id="58150-108">オブジェクトまたはアプリケーション エラーの発生源の名前を決定するのに[Error](error-object-ado.md)オブジェクトの**Source**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="58150-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="58150-109">これは、オブジェクトのクラス名またはプログラム id です。</span><span class="sxs-lookup"><span data-stu-id="58150-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="58150-110">ADO のエラー、プロパティの値になります \**ADODB.。 ObjectName*、*オブジェクト名*は、エラーを引き起こしたオブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="58150-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="58150-111">ADOX および ADO MD の場合は、値となります \**ADOX。。 ObjectName*および \**ADOMD。。 オブジェクト名は、* それぞれ。</span><span class="sxs-lookup"><span data-stu-id="58150-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="58150-112">**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。</span><span class="sxs-lookup"><span data-stu-id="58150-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="58150-113">**Error** オブジェクトの **Source** プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="58150-113">The **Source** property is read-only for **Error** objects.</span></span>


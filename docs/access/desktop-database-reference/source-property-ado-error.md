---
title: Source プロパティ (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061308"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="86dee-102">Source プロパティ (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="86dee-102">Source property (ADO Error)</span></span>


<span data-ttu-id="86dee-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="86dee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86dee-104">エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="86dee-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="86dee-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="86dee-105">Return value</span></span>

<span data-ttu-id="86dee-106">オブジェクトまたはアプリケーションの名前を示す文字列型 (**String**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="86dee-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="86dee-107">解説</span><span class="sxs-lookup"><span data-stu-id="86dee-107">Remarks</span></span>

<span data-ttu-id="86dee-108">Error オブジェクト **の Source** プロパティ [を使用](error-object-ado.md) して、最初にエラーを生成したオブジェクトまたはアプリケーションの名前を特定します。</span><span class="sxs-lookup"><span data-stu-id="86dee-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="86dee-109">これは、オブジェクトのクラス名またはプログラム ID です。</span><span class="sxs-lookup"><span data-stu-id="86dee-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="86dee-110">ADO のエラーの場合、プロパティの値は **ADODB になります。**</span><span class="sxs-lookup"><span data-stu-id="86dee-110">For errors in ADO, the property value will be **ADODB.**</span></span> <span data-ttu-id="86dee-111">*ObjectName*、 *ObjectName* は、エラーをトリガーしたオブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="86dee-111">*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="86dee-112">ADOX と ADO MD の場合、値は **ADOX になります。**</span><span class="sxs-lookup"><span data-stu-id="86dee-112">For ADOX and ADO MD, the value will be **ADOX.**</span></span> <span data-ttu-id="86dee-113">*ObjectName* と **ADOMD。**</span><span class="sxs-lookup"><span data-stu-id="86dee-113">*ObjectName* and **ADOMD.**</span></span> <span data-ttu-id="86dee-114">*それぞれ ObjectName。*</span><span class="sxs-lookup"><span data-stu-id="86dee-114">*ObjectName,* respectively.</span></span>

<span data-ttu-id="86dee-115">**Error** オブジェクトの [Source](number-property-ado.md) プロパティ、 [Number](description-property-ado.md) プロパティ、および **Description** プロパティのエラー情報に基づいて、エラーを適切に処理するためのコードを書くことができます。</span><span class="sxs-lookup"><span data-stu-id="86dee-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="86dee-116">**Error** オブジェクトの **Source** プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="86dee-116">The **Source** property is read-only for **Error** objects.</span></span>


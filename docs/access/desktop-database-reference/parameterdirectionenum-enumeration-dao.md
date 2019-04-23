---
title: parameterdirection 列挙列挙 (DAO)
TOCTitle: ParameterDirectionEnum Enumeration
ms:assetid: 3f2b91f4-a932-aca5-34a0-4002c27d6b3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192844(v=office.15)
ms:contentKeyID: 48544389
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d467f66da41559e607520a4328388c41843bc87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287991"
---
# <a name="parameterdirectionenum-enumeration-dao"></a><span data-ttu-id="ac9c6-102">parameterdirection 列挙列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="ac9c6-102">ParameterDirectionEnum enumeration (DAO)</span></span>


<span data-ttu-id="ac9c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac9c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac9c6-104">" **Direction**/方向" プロパティで、 **Parameter** オブジェクトの種類を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ac9c6-104">Used with the **Direction** property to specify the type for a **Parameter** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac9c6-105">名前</span><span class="sxs-lookup"><span data-stu-id="ac9c6-105">Name</span></span></p></th>
<th><p><span data-ttu-id="ac9c6-106">値</span><span class="sxs-lookup"><span data-stu-id="ac9c6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ac9c6-107">説明</span><span class="sxs-lookup"><span data-stu-id="ac9c6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac9c6-108">dbParamInput</span><span class="sxs-lookup"><span data-stu-id="ac9c6-108">dbParamInput</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-109">1-d</span><span class="sxs-lookup"><span data-stu-id="ac9c6-109">1</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-110">(既定値) プロシージャに情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="ac9c6-110">(Default) Passes information to the procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac9c6-111">dbParamInputOutput</span><span class="sxs-lookup"><span data-stu-id="ac9c6-111">dbParamInputOutput</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-112">1/3</span><span class="sxs-lookup"><span data-stu-id="ac9c6-112">3</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-113">プロシージャとの間で情報を受け渡します。</span><span class="sxs-lookup"><span data-stu-id="ac9c6-113">Passes information both to and from the procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac9c6-114">代わりに dbparamoutput</span><span class="sxs-lookup"><span data-stu-id="ac9c6-114">dbParamOutput</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="ac9c6-115">2</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-116">プロシージャからの情報を SQL の出力パラメーターとして返します。</span><span class="sxs-lookup"><span data-stu-id="ac9c6-116">Returns information from the procedure as an output parameter in SQL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac9c6-117">は dbparamreturnvalue</span><span class="sxs-lookup"><span data-stu-id="ac9c6-117">dbParamReturnValue</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-118">2/4</span><span class="sxs-lookup"><span data-stu-id="ac9c6-118">4</span></span></p></td>
<td><p><span data-ttu-id="ac9c6-119">プロシージャからの戻り値を渡します。</span><span class="sxs-lookup"><span data-stu-id="ac9c6-119">Passes the return value from a procedure.</span></span></p></td>
</tr>
</tbody>
</table>


---
title: GetPermissions メソッド (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b7e6603d8da5bafc7a479cb8bfe94577a0679bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478665"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="8d209-102">GetPermissions メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8d209-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="8d209-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d209-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="8d209-104">グループまたはユーザーのオブジェクトまたはオブジェクト コンテナーに対する権限を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d209-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d209-105">構文</span><span class="sxs-lookup"><span data-stu-id="8d209-105">Syntax</span></span>

<span data-ttu-id="8d209-106">*戻り値* = *<*。GetPermissions (*名前*、 *ObjectType* \[、*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="8d209-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="8d209-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d209-107">Return Value</span></span>

<span data-ttu-id="8d209-p101">グループまたはユーザーが、そのオブジェクトに持つ権限を含むビットマスクを示す長整数型 ( **Long** ) の値を取得します。この値は、1 つ以上の [RightsEnum](rightsenum.md) 定数です。</span><span class="sxs-lookup"><span data-stu-id="8d209-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d209-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d209-110">Parameters</span></span>

  - <span data-ttu-id="8d209-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="8d209-111">*Name*</span></span>

  - <span data-ttu-id="8d209-112">権限を設定するオブジェクトの名前を示すバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d209-112">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="8d209-113">オブジェクト コンテナーの権限を取得する場合は、null 値に*名前*を設定します。</span><span class="sxs-lookup"><span data-stu-id="8d209-113">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="8d209-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="8d209-114">*ObjectType*</span></span>

  - <span data-ttu-id="8d209-115">権限を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d209-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="8d209-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="8d209-116">*ObjectTypeId*</span></span>

  - <span data-ttu-id="8d209-117">省略可能。</span><span class="sxs-lookup"><span data-stu-id="8d209-117">Optional.</span></span> <span data-ttu-id="8d209-118">OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="8d209-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="8d209-119">**AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="8d209-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

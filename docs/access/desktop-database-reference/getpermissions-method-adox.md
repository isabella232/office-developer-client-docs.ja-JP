---
title: getpermissions メソッド (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292245"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="695ef-102">getpermissions メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="695ef-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="695ef-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="695ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="695ef-104">グループまたはユーザーのオブジェクトまたはオブジェクト コンテナーに対する権限を取得します。</span><span class="sxs-lookup"><span data-stu-id="695ef-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="695ef-105">構文</span><span class="sxs-lookup"><span data-stu-id="695ef-105">Syntax</span></span>

<span data-ttu-id="695ef-106">*戻り* = \*\* ます。getpermissions (*Name*、 *ObjectType* \[、*objecttypeid*\])</span><span class="sxs-lookup"><span data-stu-id="695ef-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="695ef-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="695ef-107">Return value</span></span>

<span data-ttu-id="695ef-p101">グループまたはユーザーが、そのオブジェクトに持つ権限を含むビットマスクを示す長整数型 ( **Long** ) の値を取得します。この値は、1 つ以上の [RightsEnum](rightsenum.md) 定数です。</span><span class="sxs-lookup"><span data-stu-id="695ef-p101">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object. This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="695ef-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="695ef-110">Parameters</span></span>

|<span data-ttu-id="695ef-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="695ef-111">Parameter</span></span>|<span data-ttu-id="695ef-112">説明</span><span class="sxs-lookup"><span data-stu-id="695ef-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="695ef-113">*名前*</span><span class="sxs-lookup"><span data-stu-id="695ef-113">*Name*</span></span> |<span data-ttu-id="695ef-p102">権限を設定するオブジェクトの名前を示すバリアント型 (**Variant**) の値を指定します。オブジェクト コンテナーの権限を取得する場合は、*Name* を Null 値に設定します。</span><span class="sxs-lookup"><span data-stu-id="695ef-p102">A **Variant** value that specifies the name of the object for which to set permissions. Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="695ef-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="695ef-116">*ObjectType*</span></span> |<span data-ttu-id="695ef-117">権限を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="695ef-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="695ef-118">*objecttypeid*</span><span class="sxs-lookup"><span data-stu-id="695ef-118">*ObjectTypeId*</span></span> |<span data-ttu-id="695ef-p103">省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="695ef-p103">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|


---
title: SetPermissions メソッド (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9ea1c08223282654af636326ba9a8c2bfe70e67
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949601"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="37fae-102">SetPermissions メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="37fae-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="37fae-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="37fae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37fae-104">グループまたはユーザーのオブジェクトに対する権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="37fae-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fae-105">構文</span><span class="sxs-lookup"><span data-stu-id="37fae-105">Syntax</span></span>

<span data-ttu-id="37fae-106">*<*。SetPermissions*名*、*オブジェクト タイプ*、*アクション*、ユーザーの*権利* \[、*継承*\] \[、*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="37fae-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="37fae-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37fae-107">Parameters</span></span>

|<span data-ttu-id="37fae-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37fae-108">Parameter</span></span>|<span data-ttu-id="37fae-109">説明</span><span class="sxs-lookup"><span data-stu-id="37fae-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="37fae-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="37fae-110">*Name*</span></span> |<span data-ttu-id="37fae-111">権限を設定するオブジェクトの名前を指定する文字列型 ( **String** ) の値。</span><span class="sxs-lookup"><span data-stu-id="37fae-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="37fae-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="37fae-112">*ObjectType*</span></span> |<span data-ttu-id="37fae-113">**ObjectTypeEnum** 定数のいずれかである長整数型 ( [Long](objecttypeenum.md) ) の値。権限を与えるオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="37fae-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="37fae-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="37fae-114">*Action*</span></span> |<span data-ttu-id="37fae-115">**ActionEnum** 定数のいずれかである長整数型 ( [Long](actionenum.md) ) の値。権限を設定するときに実行するアクションの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="37fae-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="37fae-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="37fae-116">*Rights*</span></span> |<span data-ttu-id="37fae-117">1 つ以上の **RightsEnum** 定数のビットマスクである長整数型 ( [Long](rightsenum.md) ) の値。設定する権限を示します。</span><span class="sxs-lookup"><span data-stu-id="37fae-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="37fae-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="37fae-118">*Inherit*</span></span> |<span data-ttu-id="37fae-p101">省略可能です。**InheritTypeEnum** 定数のいずれかである長整数型 ( [Long](inherittypeenum.md) ) の値。オブジェクトによるこれらの権限の継承方法を指定します。既定値は **adInheritNone** です。</span><span class="sxs-lookup"><span data-stu-id="37fae-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="37fae-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="37fae-122">*ObjectTypeId*</span></span> |<span data-ttu-id="37fae-123">省略可能。</span><span class="sxs-lookup"><span data-stu-id="37fae-123">Optional.</span></span> <span data-ttu-id="37fae-124">OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="37fae-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="37fae-125">**AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="37fae-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="37fae-126">解説</span><span class="sxs-lookup"><span data-stu-id="37fae-126">Remarks</span></span>

<span data-ttu-id="37fae-127">プロバイダーがグループまたはユーザーのアクセス権の設定をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="37fae-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="37fae-128">**SetPermissions**を呼び出すときにアクションを**adAccessRevoke**に設定する*権限*のパラメーターの設定をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="37fae-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="37fae-129">*Rights*パラメーターで指定されている権限を有効にする場合、*アクション*を**adAccessRevoke**に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="37fae-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>



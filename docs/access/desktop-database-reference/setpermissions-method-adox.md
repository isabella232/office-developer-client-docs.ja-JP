---
title: SetPermissions メソッド (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314582"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="0f8e5-102">SetPermissions メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0f8e5-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="0f8e5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f8e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f8e5-104">グループまたはユーザーのオブジェクトに対する権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8e5-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f8e5-105">Syntax</span></span>

<span data-ttu-id="0f8e5-106">*grouporuser*。SetPermissions*Name*、 *ObjectType*、 *Action*、 *Rights* \[、*Inherit* \] \[、*objecttypeid*\]</span><span class="sxs-lookup"><span data-stu-id="0f8e5-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="0f8e5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f8e5-107">Parameters</span></span>

|<span data-ttu-id="0f8e5-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f8e5-108">Parameter</span></span>|<span data-ttu-id="0f8e5-109">説明</span><span class="sxs-lookup"><span data-stu-id="0f8e5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0f8e5-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-110">*Name*</span></span> |<span data-ttu-id="0f8e5-111">権限を設定するオブジェクトの名前を指定する文字列型 ( **String** ) の値。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="0f8e5-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-112">*ObjectType*</span></span> |<span data-ttu-id="0f8e5-113">**ObjectTypeEnum** 定数のいずれかである長整数型 ( [Long](objecttypeenum.md) ) の値。権限を与えるオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="0f8e5-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-114">*Action*</span></span> |<span data-ttu-id="0f8e5-115">**ActionEnum** 定数のいずれかである長整数型 ( [Long](actionenum.md) ) の値。権限を設定するときに実行するアクションの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="0f8e5-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-116">*Rights*</span></span> |<span data-ttu-id="0f8e5-117">1 つ以上の **RightsEnum** 定数のビットマスクである長整数型 ( [Long](rightsenum.md) ) の値。設定する権限を示します。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="0f8e5-118">*Inherit*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-118">*Inherit*</span></span> |<span data-ttu-id="0f8e5-p101">省略可能です。**InheritTypeEnum** 定数のいずれかである長整数型 ( [Long](inherittypeenum.md) ) の値。オブジェクトによるこれらの権限の継承方法を指定します。既定値は **adInheritNone** です。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-p101">Optional. A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions. The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="0f8e5-122">*objecttypeid*</span><span class="sxs-lookup"><span data-stu-id="0f8e5-122">*ObjectTypeId*</span></span> |<span data-ttu-id="0f8e5-p102">省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-p102">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0f8e5-126">注釈</span><span class="sxs-lookup"><span data-stu-id="0f8e5-126">Remarks</span></span>

<span data-ttu-id="0f8e5-127">プロバイダーがグループまたはユーザーのアクセス権の設定をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="0f8e5-p103">**SetPermissions** を呼び出すときに、Actions を **adAccessRevoke** に設定すると、*Rights* パラメーターのすべての設定が無効になります。*Rights* パラメーターで指定した権限を有効にする場合は、*Actions* を **adAccessRevoke** に設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="0f8e5-p103">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter. Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>



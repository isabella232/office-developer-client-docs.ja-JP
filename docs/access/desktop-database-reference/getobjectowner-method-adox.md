---
title: GetObjectOwner メソッド (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6961cb1de192e480ca68d9688105600ac85c69c9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874217"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="09c94-102">GetObjectOwner メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="09c94-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="09c94-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="09c94-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="09c94-104">[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。</span><span class="sxs-lookup"><span data-stu-id="09c94-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09c94-105">構文</span><span class="sxs-lookup"><span data-stu-id="09c94-105">Syntax</span></span>

<span data-ttu-id="09c94-106">*所有者* = *カタログ*です。GetObjectOwner (*オブジェクト名*、*オブジェクト タイプ* \[、*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="09c94-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="09c94-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="09c94-107">Return value</span></span>

<span data-ttu-id="09c94-108">オブジェクトを所有する **User** または [Group](name-property-adox.md) の [Name プロパティ (ADOX)](user-object-adox.md) を指定する文字列型 ( [String](group-object-adox.md) ) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="09c94-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="09c94-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="09c94-109">Parameters</span></span>

  - <span data-ttu-id="09c94-110">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="09c94-110">*ObjectName*</span></span>

  - <span data-ttu-id="09c94-111">所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="09c94-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="09c94-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="09c94-112">*ObjectType*</span></span>

  - <span data-ttu-id="09c94-113">所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="09c94-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="09c94-114">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="09c94-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="09c94-115">省略可能。</span><span class="sxs-lookup"><span data-stu-id="09c94-115">Optional.</span></span> <span data-ttu-id="09c94-116">OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="09c94-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="09c94-117">**AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="09c94-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c94-118">解説</span><span class="sxs-lookup"><span data-stu-id="09c94-118">Remarks</span></span>

<span data-ttu-id="09c94-119">プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="09c94-119">An error will occur if the provider does not support returning object owners.</span></span>


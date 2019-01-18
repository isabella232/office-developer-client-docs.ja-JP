---
title: GetObjectOwner メソッド (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710732"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="3749a-102">GetObjectOwner メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3749a-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="3749a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3749a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3749a-104">[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。</span><span class="sxs-lookup"><span data-stu-id="3749a-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3749a-105">構文</span><span class="sxs-lookup"><span data-stu-id="3749a-105">Syntax</span></span>

<span data-ttu-id="3749a-106">*所有者* = *カタログ*です。GetObjectOwner (*オブジェクト名*、*オブジェクト タイプ* \[、*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="3749a-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="3749a-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="3749a-107">Return value</span></span>

<span data-ttu-id="3749a-108">オブジェクトを所有する **User** または [Group](name-property-adox.md) の [Name プロパティ (ADOX)](user-object-adox.md) を指定する文字列型 ( [String](group-object-adox.md) ) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="3749a-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3749a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3749a-109">Parameters</span></span>

|<span data-ttu-id="3749a-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3749a-110">Parameter</span></span>|<span data-ttu-id="3749a-111">説明</span><span class="sxs-lookup"><span data-stu-id="3749a-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3749a-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="3749a-112">*ObjectName*</span></span> |<span data-ttu-id="3749a-113">所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3749a-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="3749a-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="3749a-114">*ObjectType*</span></span> |<span data-ttu-id="3749a-115">所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3749a-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="3749a-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="3749a-116">*ObjectTypeId*</span></span> |<span data-ttu-id="3749a-117">省略可能。</span><span class="sxs-lookup"><span data-stu-id="3749a-117">Optional.</span></span> <span data-ttu-id="3749a-118">OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="3749a-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="3749a-119">**AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="3749a-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3749a-120">解説</span><span class="sxs-lookup"><span data-stu-id="3749a-120">Remarks</span></span>

<span data-ttu-id="3749a-121">プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3749a-121">An error will occur if the provider does not support returning object owners.</span></span>


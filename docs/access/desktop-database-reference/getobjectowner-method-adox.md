---
title: getobjectowner メソッドメソッド (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292259"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="34e9c-102">getobjectowner メソッドメソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="34e9c-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="34e9c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="34e9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34e9c-104">[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。</span><span class="sxs-lookup"><span data-stu-id="34e9c-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34e9c-105">構文</span><span class="sxs-lookup"><span data-stu-id="34e9c-105">Syntax</span></span>

<span data-ttu-id="34e9c-106">*所有者* = *カタログ*。getobjectowner メソッド (*ObjectName*、 *ObjectType* \[、*objecttypeid*\])</span><span class="sxs-lookup"><span data-stu-id="34e9c-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="34e9c-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="34e9c-107">Return value</span></span>

<span data-ttu-id="34e9c-108">オブジェクトを所有する [User](user-object-adox.md) または [Group](group-object-adox.md) の [Name プロパティ (ADOX)](name-property-adox.md) を指定する文字列型 (**String**) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="34e9c-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="34e9c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34e9c-109">Parameters</span></span>

|<span data-ttu-id="34e9c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34e9c-110">Parameter</span></span>|<span data-ttu-id="34e9c-111">説明</span><span class="sxs-lookup"><span data-stu-id="34e9c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="34e9c-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="34e9c-112">*ObjectName*</span></span> |<span data-ttu-id="34e9c-113">所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="34e9c-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="34e9c-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="34e9c-114">*ObjectType*</span></span> |<span data-ttu-id="34e9c-115">所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="34e9c-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="34e9c-116">*objecttypeid*</span><span class="sxs-lookup"><span data-stu-id="34e9c-116">*ObjectTypeId*</span></span> |<span data-ttu-id="34e9c-p101">省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="34e9c-p101">Optional. A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification. This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="34e9c-120">注釈</span><span class="sxs-lookup"><span data-stu-id="34e9c-120">Remarks</span></span>

<span data-ttu-id="34e9c-121">プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="34e9c-121">An error will occur if the provider does not support returning object owners.</span></span>


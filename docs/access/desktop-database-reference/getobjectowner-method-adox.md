---
title: GetObjectOwner メソッド (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6c2432370f2480484cf1165249bc8573b27372
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603113"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="e883f-102">GetObjectOwner メソッド (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e883f-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="e883f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e883f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e883f-104">[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。</span><span class="sxs-lookup"><span data-stu-id="e883f-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e883f-105">構文</span><span class="sxs-lookup"><span data-stu-id="e883f-105">Syntax</span></span>

<span data-ttu-id="e883f-106">*所有者* = *カタログ*です。GetObjectOwner (*オブジェクト名*、*オブジェクト タイプ* \[、*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="e883f-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="e883f-107"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e883f-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e883f-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="e883f-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e883f-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e883f-109">Return value</span></span>
>>>>>>> <span data-ttu-id="e883f-110">master</span><span class="sxs-lookup"><span data-stu-id="e883f-110">master</span></span>

<span data-ttu-id="e883f-111">オブジェクトを所有する **User** または [Group](name-property-adox.md) の [Name プロパティ (ADOX)](user-object-adox.md) を指定する文字列型 ( [String](group-object-adox.md) ) の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e883f-111">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e883f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e883f-112">Parameters</span></span>

  - <span data-ttu-id="e883f-113">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="e883f-113">*ObjectName*</span></span>

  - <span data-ttu-id="e883f-114">所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e883f-114">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="e883f-115">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="e883f-115">*ObjectType*</span></span>

  - <span data-ttu-id="e883f-116">所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e883f-116">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="e883f-117">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="e883f-117">*ObjectTypeId*</span></span>

  - <span data-ttu-id="e883f-118">省略可能。</span><span class="sxs-lookup"><span data-stu-id="e883f-118">Optional.</span></span> <span data-ttu-id="e883f-119">OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。</span><span class="sxs-lookup"><span data-stu-id="e883f-119">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="e883f-120">**AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。</span><span class="sxs-lookup"><span data-stu-id="e883f-120">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e883f-121">解説</span><span class="sxs-lookup"><span data-stu-id="e883f-121">Remarks</span></span>

<span data-ttu-id="e883f-122">プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e883f-122">An error will occur if the provider does not support returning object owners.</span></span>


---
title: ParentCatalog プロパティ (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603414"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="9d583-102">ParentCatalog プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9d583-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="9d583-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d583-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9d583-104">プロバイダー固有のプロパティへのアクセスを提供する、テーブルまたは列の親カタログを指定します。</span><span class="sxs-lookup"><span data-stu-id="9d583-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

<span data-ttu-id="9d583-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9d583-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="9d583-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="9d583-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="9d583-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="9d583-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="9d583-108">master</span><span class="sxs-lookup"><span data-stu-id="9d583-108">master</span></span>

<span data-ttu-id="9d583-p101">[Catalog](catalog-object-adox.md) オブジェクトを設定および取得します。 **ParentCatalog** を開かれた **Catalog** に設定すると、テーブルまたは列を **Catalog** コレクションに追加する前に、プロバイダー固有のプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9d583-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d583-111">解説</span><span class="sxs-lookup"><span data-stu-id="9d583-111">Remarks</span></span>

<span data-ttu-id="9d583-p102">データ プロバイダーの中には、作成時 (テーブルまたは列が **Catalog** コレクションに追加されるとき) のみプロバイダー固有のプロパティ値を設定できるものがあります。 **Catalog** にオブジェクトを追加する前に、これらのプロパティにアクセスするには、あらかじめ **ParentCatalog** プロパティで **Catalog** を指定しておきます。</span><span class="sxs-lookup"><span data-stu-id="9d583-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="9d583-114">テーブルまたは列を **ParentCatalog** 以外の **Catalog** に追加すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9d583-114">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


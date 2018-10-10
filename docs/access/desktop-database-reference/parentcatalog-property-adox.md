---
title: ParentCatalog プロパティ (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 644312ab6b51b1b084d2d11f52117cece7afdf0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476709"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="f7d7b-102">ParentCatalog プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f7d7b-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="f7d7b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7d7b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7d7b-104">プロバイダー固有のプロパティへのアクセスを提供する、テーブルまたは列の親カタログを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7d7b-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f7d7b-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="f7d7b-105">Settings and Return Values</span></span>

<span data-ttu-id="f7d7b-p101">[Catalog](catalog-object-adox.md) オブジェクトを設定および取得します。 **ParentCatalog** を開かれた **Catalog** に設定すると、テーブルまたは列を **Catalog** コレクションに追加する前に、プロバイダー固有のプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f7d7b-p101">Sets and returns a [Catalog](catalog-object-adox.md) object. Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d7b-108">解説</span><span class="sxs-lookup"><span data-stu-id="f7d7b-108">Remarks</span></span>

<span data-ttu-id="f7d7b-p102">データ プロバイダーの中には、作成時 (テーブルまたは列が **Catalog** コレクションに追加されるとき) のみプロバイダー固有のプロパティ値を設定できるものがあります。 **Catalog** にオブジェクトを追加する前に、これらのプロパティにアクセスするには、あらかじめ **ParentCatalog** プロパティで **Catalog** を指定しておきます。</span><span class="sxs-lookup"><span data-stu-id="f7d7b-p102">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection). To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="f7d7b-111">テーブルまたは列を **ParentCatalog** 以外の **Catalog** に追加すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f7d7b-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


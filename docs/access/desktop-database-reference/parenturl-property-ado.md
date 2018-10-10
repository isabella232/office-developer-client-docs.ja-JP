---
title: ParentURL プロパティ (ADO)
TOCTitle: ParentURL Property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fb5e8683bcf7ebe0905b21f169f71834ed424e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479599"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="36629-102">ParentURL プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="36629-102">ParentURL Property (ADO)</span></span>

<span data-ttu-id="36629-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="36629-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36629-104">現在の [Record](record-object-ado.md) オブジェクトの親 **Record** を示す絶対 URL 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="36629-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="36629-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="36629-105">Return Value</span></span>

<span data-ttu-id="36629-106">親 **Record** の URL を示す文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="36629-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="36629-107">解説</span><span class="sxs-lookup"><span data-stu-id="36629-107">Remarks</span></span>

<span data-ttu-id="36629-p101">**ParentURL** プロパティは、 **Record** オブジェクトを開くために使用されるソースに依存します。たとえば、 **ActiveConnection** プロパティによって参照されるディレクトリの相対パスを含むソースを使用して [Record](activeconnection-property-ado.md) を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="36629-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="36629-p102">ここで、"second" が "first" の下のフォルダーであるとします。 **Record** オブジェクトを開くには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="36629-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="36629-112">**ParentURL**プロパティの値は、 **ParentURL**プロパティは、"https://first"、 **ActiveConnection**と同じです。</span><span class="sxs-lookup"><span data-stu-id="36629-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="36629-113">ソースの絶対 URL を次のように、場合もあります"https://first/second"です。</span><span class="sxs-lookup"><span data-stu-id="36629-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="36629-114">**ParentURL**プロパティでは、"https://first"、上のレベルです。</span><span class="sxs-lookup"><span data-stu-id="36629-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="36629-115">**ParentURL**プロパティでは、"https://first"、「秒」の上のレベルです。</span><span class="sxs-lookup"><span data-stu-id="36629-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="36629-116">次のような場合、このプロパティは Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="36629-116">This property may be a null value if:</span></span>

- <span data-ttu-id="36629-117">現在のレコードに親がない場合 ( **Record** オブジェクトがディレクトリのルートを表す場合など)</span><span class="sxs-lookup"><span data-stu-id="36629-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="36629-118">**Record** オブジェクトが URL で指定できないエンティティである場合</span><span class="sxs-lookup"><span data-stu-id="36629-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="36629-119">このプロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="36629-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="36629-p104">[!メモ] このプロパティは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) などのドキュメント ソース プロバイダーでのみサポートされます。詳細については、「 [レコードおよびプロバイダー提供のフィールド](records-and-provider-supplied-fields.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36629-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="36629-122">[!メモ] http 体系を使用している URL は、Microsoft OLE DB Provider for Internet Publishing を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36629-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="36629-123">詳細については、「 [絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36629-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="36629-124">[!メモ] 現在のレコードに ADO **Recordset** のデータ レコードが含まれている場合、 **ParentURL** プロパティにアクセスすると、URL を取得できないことを示す実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="36629-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


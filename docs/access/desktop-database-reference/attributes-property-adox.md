---
title: Attributes プロパティ (ADOX)
TOCTitle: Attributes property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14a4c719723767be8cb8e7e2f8ed02b5d2d4a143
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698170"
---
# <a name="attributes-property-adox"></a><span data-ttu-id="2b3ae-102">Attributes プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2b3ae-102">Attributes property (ADOX)</span></span>


<span data-ttu-id="2b3ae-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2b3ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b3ae-104">列の属性を示します。</span><span class="sxs-lookup"><span data-stu-id="2b3ae-104">Describes column characteristics.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2b3ae-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="2b3ae-105">Settings and return values</span></span>

<span data-ttu-id="2b3ae-p101">長整数型 ( **Long** ) の値を設定または返します。この値は [Column](column-object-adox.md) オブジェクトによって表されるテーブルの属性を指定し、 [ColumnAttributesEnum](columnattributesenum.md) 定数を組み合わせることができます。既定値は 0 (ゼロ) です。 **adColFixed** でも **adColNullable** でもありません。</span><span class="sxs-lookup"><span data-stu-id="2b3ae-p101">Sets or returns a **Long** value. The value specifies characteristics of the table represented by the [Column](column-object-adox.md) object and can be a combination of [ColumnAttributesEnum](columnattributesenum.md) constants. The default value is zero (0), which is neither **adColFixed** nor **adColNullable**.</span></span>


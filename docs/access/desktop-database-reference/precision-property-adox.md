---
title: Precision プロパティ (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e64a7166b73c5fca1fa7f5e0b63fabeec715c52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927502"
---
# <a name="precision-property-adox"></a><span data-ttu-id="63670-102">Precision プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="63670-102">Precision property (ADOX)</span></span>


<span data-ttu-id="63670-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="63670-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63670-104">列のデータ値の最大桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="63670-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="63670-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="63670-105">Settings and return values</span></span>

<span data-ttu-id="63670-p101">**Type** プロパティが数値型の場合に、列のデータ値の最大桁数を表す長整数型 ( [Long](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) ) の値を設定および取得します。数値型以外のデータ型の場合、 **Precision** プロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="63670-p101">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type. **Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="63670-108">解説</span><span class="sxs-lookup"><span data-stu-id="63670-108">Remarks</span></span>

<span data-ttu-id="63670-109">既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="63670-109">The default value is zero (0).</span></span>

<span data-ttu-id="63670-110">このプロパティは、[Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="63670-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>


---
title: プロパティ (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307330"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="34a64-102">プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="34a64-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="34a64-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a64-p101">次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="34a64-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a64-106">構文</span><span class="sxs-lookup"><span data-stu-id="34a64-106">Syntax</span></span>

<span data-ttu-id="34a64-107">*式*。仕訳</span><span class="sxs-lookup"><span data-stu-id="34a64-107">*expression* .Filter</span></span>

<span data-ttu-id="34a64-108">\*式\***Recordset2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="34a64-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a64-109">注釈</span><span class="sxs-lookup"><span data-stu-id="34a64-109">Remarks</span></span>

<span data-ttu-id="34a64-110">設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。</span><span class="sxs-lookup"><span data-stu-id="34a64-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="34a64-111">**Filter** プロパティを使用して、ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの **Recordset** オブジェクトにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="34a64-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="34a64-112">**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。</span><span class="sxs-lookup"><span data-stu-id="34a64-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="34a64-113">米国版の Microsoft Access データベースエンジンを使用していない場合でも、日付を含むフィールドにフィルターを適用する場合は米国の日付形式 (月-日-年) を使用します (この場合は文字列を連結することによって日付をアセンブルする必要があります。たとえば、strmonth & "-" & strday & "-" & strday)。</span><span class="sxs-lookup"><span data-stu-id="34a64-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="34a64-114">この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="34a64-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="34a64-115">多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="34a64-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="34a64-116">プロパティに整数以外の値を連結した文字列を設定した場合、システムパラメーターにコンマ (たとえば、strfilter = "PRICE \> " & lngPrice, and lngPrice = 125, 50) などの非10進文字を指定しようとすると、エラーが発生します。次の**Recordset**を開きます。</span><span class="sxs-lookup"><span data-stu-id="34a64-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="34a64-117">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="34a64-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


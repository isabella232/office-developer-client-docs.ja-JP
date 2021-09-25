---
title: Recordset2.Filter プロパティ (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 757aec47564e6462bf543e408825367ef26b775c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605982"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter プロパティ (DAO)


**適用先**: Access 2013、Office 2013

次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。

## <a name="syntax"></a>構文

*式* .Filter

*式* Recordset2 オブジェクトを **返す** 式。

## <a name="remarks"></a>注釈

設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。


            **Filter** プロパティを使用して、ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの **Recordset** オブジェクトにフィルターを適用します。


            **Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。

日付が含まれたフィールドをフィルター処理するときは、米国版の Microsoft Access データベース エンジンを使用していない場合でも、米国の日付形式 (month-day-year) を使用します (この場合、連結文字列を使用して日付を構成する必要があり、たとえば、strMonth & "-" & strDay & "-" & strYear のように設定します)。 この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。

多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。

このプロパティを文字列と非整数値を連結した値に設定し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strFilter = "PRICE \> " & lngPrice で lngPrice = 125,50)、次の **Recordset** オブジェクトを開こうとするとエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。


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
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720353"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。フィルター

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。

ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトにフィルターを適用するのにには、 **Filter**プロパティを使用します。

**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。

(月-日-年) 米国の日付形式を使用して、米国版の Microsoft Access データベース エンジンを使用していない場合でも、日付を含むフィールドをフィルターするとき (場合に、たとえば、strMonth & の文字列を連結することにより任意の日付をアセンブリする必要が"-"& strDay &"-"& strYear)。 この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。

多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。

非 – 整数値と連結した文字列にプロパティを設定して、システム パラメーター、米国以外の小数点の記号、カンマなどを指定するかどうか (たとえば、strFilter ="価格\>"& lngPrice でと lngPrice = 125,50)、しようとするときにエラーが発生しました。次の**レコード セット**を開きます。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。


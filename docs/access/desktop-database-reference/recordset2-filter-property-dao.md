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
ms.openlocfilehash: ba5b43f6b0012e45c3cb4af662454ef76eab9194
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479008"
---
# <a name="recordset2filter-property-dao"></a>Recordset2.Filter プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。フィルター

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。

ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトにフィルターを適用するのにには、 **Filter**プロパティを使用します。

**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。

(月-日-年) 米国の日付形式を使用して、米国版の Microsoft Access データベース エンジンを使用していない場合でも、日付を含むフィールドをフィルターするとき (文字列、たとえば、strMonth を連結することにより、任意の日付をアセンブリする必要が場合 &"-"& strDay &"、"& strYear)。 この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。

多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。

非 – 整数値と連結した文字列にプロパティを設定して、システム パラメーター、米国以外の小数点の記号、カンマなどを指定するかどうか (たとえば、strFilter ="価格\>"& lngPrice でと lngPrice = 125,50)、しようとするときにエラーが発生しました。次の**レコード セット**を開きます。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。


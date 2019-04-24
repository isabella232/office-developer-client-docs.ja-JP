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
# <a name="recordset2filter-property-dao"></a>プロパティ (DAO)


**適用先:** Access 2013、Office 2013

次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。

## <a name="syntax"></a>構文

*式*。仕訳

*式***Recordset2**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。

**Filter** プロパティを使用して、ダイナセット タイプ、スナップショット タイプ、または前方スクロール タイプの **Recordset** オブジェクトにフィルターを適用します。

**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。

米国版の Microsoft Access データベースエンジンを使用していない場合でも、日付を含むフィールドにフィルターを適用する場合は米国の日付形式 (月-日-年) を使用します (この場合は文字列を連結することによって日付をアセンブルする必要があります。たとえば、strmonth & "-" & strday & "-" & strday)。 この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。

多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。

プロパティに整数以外の値を連結した文字列を設定した場合、システムパラメーターにコンマ (たとえば、strfilter = "PRICE \> " & lngPrice, and lngPrice = 125, 50) などの非10進文字を指定しようとすると、エラーが発生します。次の**Recordset**を開きます。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。


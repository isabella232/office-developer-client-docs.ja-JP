---
title: Recordset.Filter プロパティ (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 7ab090dd6cf0b6e2676cf05907ac77c438f22652
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711708"
---
# <a name="recordsetfilter-property-dao"></a>Recordset.Filter プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

次に開く **Recordset** オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。フィルター

*式***レコード セット**オブジェクトを返す式です。

## <a name="remarks"></a>注釈

設定値または戻り値は、SQL ステートメントの WHERE 句から予約語 WHERE を除いた部分を含む文字列データ型 (String) の値です。

ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトにフィルターを適用するのにには、 **Filter**プロパティを使用します。

**Filter** プロパティを使用すると、既存の **Recordset** オブジェクトに基づいて新しい **Recordset** オブジェクトを開くときに、既存のオブジェクトから取得するレコードを制限できます。

(月-日-年) 米国の日付形式を使用して、米国版の Microsoft Access データベース エンジンを使用していない場合でも、日付を含むフィールドをフィルターするとき (場合に、たとえば、strMonth & の文字列を連結することにより任意の日付をアセンブリする必要が"-"& strDay &"-"& strYear)。 この形式で構成されていない場合、データが予期したとおりにフィルター処理されないことがあります。

多くの場合、WHERE 句が含まれた SQL ステートメントを使用すると、より短時間で新しい **Recordset** オブジェクトを開くことができます。

非 – 整数値と連結した文字列にプロパティを設定して、システム パラメーター、米国以外の小数点の記号、カンマなどを指定するかどうか (たとえば、strFilter ="価格\>"& lngPrice でと lngPrice = 125,50)、しようとするときにエラーが発生しました。次の**レコード セット**を開きます。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。

## <a name="example"></a>例

次の例は、 Filter プロパティを使用して、以降に開かれる Recordset に含めるレコードを決定する方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```

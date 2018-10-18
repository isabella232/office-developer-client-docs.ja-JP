---
<<<<<<< ヘッド タイトル: Count プロパティ (ADO) TOCTitle: Count プロパティ (ADO) === タイトル: Count プロパティ (ADO) TOCTitle: Count プロパティ (ADO)
>>>>>>> マスターの ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15) ms:contentKeyID: 48547253 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="count-property-ado"></a>Count プロパティ (ADO)
=======
# <a name="count-property-ado"></a>Count プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

コレクション内のオブジェクト数を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。

コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。

**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。


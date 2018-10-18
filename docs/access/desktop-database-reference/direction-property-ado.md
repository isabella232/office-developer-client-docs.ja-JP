---
<<<<<<< ヘッド タイトル: 方向プロパティ (ADO) TOCTitle: 方向プロパティ (ADO) === タイトル: Direction プロパティ (ADO) TOCTitle: Direction プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="direction-property-ado"></a>Direction プロパティ (ADO)
=======
# <a name="direction-property-ado"></a>Direction プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。

## <a name="remarks"></a>解説

**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。

プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。


---
<<<<<<< ヘッド タイトル: RowPosition プロパティ (ADO) TOCTitle: RowPosition プロパティ (ADO) === タイトル: RowPosition プロパティ (ADO) TOCTitle: RowPosition プロパティ (ADO)
>>>>>>> マスターの ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="rowposition-property-ado"></a>RowPosition プロパティ (ADO)
=======
# <a name="rowposition-property-ado"></a>RowPosition プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013



**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。 使用すると**に\_RowPosition** **RowPosition**オブジェクトを設定するには、結果の**Recordset**オブジェクトでは、現在の行を特定するのには**RowPosition**オブジェクトを使用します。

値の取得および設定が可能です。

## <a name="syntax"></a>構文

HRESULT get\_RowPosition (\[、戻り値を\]IUnknown\* \* ppRowPos)。

HRESULT に\_RowPosition (\[の\]IUnknown\* pRowPos)。

## <a name="parameters"></a>パラメーター

  - *ppRowPos*

  - OLE DB **RowPosition** オブジェクトを指すポインター。

  - *PRowPos*

  - OLE DB **RowPosition** オブジェクト。

<<<<<<< ヘッド
## <a name="return-values"></a>戻り値
=======
## <a name="return-values"></a>戻り値
>>>>>>> master

このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。

## <a name="remarks"></a>解説

このプロパティを設定したときに、 **RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。

## <a name="applies-to"></a>対象

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)


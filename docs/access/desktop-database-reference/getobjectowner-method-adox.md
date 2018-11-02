---
title: GetObjectOwner メソッド (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927816"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner メソッド (ADOX)


**適用されます**Access 2013、Office 2013。


[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。

## <a name="syntax"></a>構文

*所有者* = *カタログ*です。GetObjectOwner (*オブジェクト名*、*オブジェクト タイプ* \[、*ObjectTypeId*\])

## <a name="return-value"></a>戻り値

オブジェクトを所有する **User** または [Group](name-property-adox.md) の [Name プロパティ (ADOX)](user-object-adox.md) を指定する文字列型 ( [String](group-object-adox.md) ) の値を取得します。

## <a name="parameters"></a>パラメーター

  - *ObjectName*

  - 所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。

  - *ObjectType*

  - 所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。

  - *ObjectTypeId*

  - 省略可能。 OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。 **AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。

## <a name="remarks"></a>解説

プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。


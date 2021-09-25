---
title: GetObjectOwner メソッド (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 215546377e085dfb1385b2f00ed882b9d3e85179
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568965"
---
# <a name="getobjectowner-method-adox"></a>GetObjectOwner メソッド (ADOX)

**適用先:** Access 2013、Office 2013

[Catalog](catalog-object-adox.md) 内のオブジェクトの所有者を返します。

## <a name="syntax"></a>構文

*所有者*  = *カタログ*.GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>戻り値

オブジェクトを所有する [User](user-object-adox.md) または [Group](group-object-adox.md) の [Name プロパティ (ADOX)](name-property-adox.md) を指定する文字列型 (**String**) の値を取得します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ObjectName* |所有者を取得するオブジェクトの名前を示す文字列型 ( **String** ) の値を指定します。|
|*ObjectType* |所有者を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。|
|*ObjectTypeId* |省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。|

## <a name="remarks"></a>注釈

プロバイダーがオブジェクトの所有者の取得をサポートしていない場合は、エラーが発生します。


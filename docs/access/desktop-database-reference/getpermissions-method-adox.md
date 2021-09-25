---
title: GetPermissions メソッド (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9cf664e1244df6eea74f447aded7b8a8fcf0350e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594245"
---
# <a name="getpermissions-method-adox"></a>GetPermissions メソッド (ADOX)

**適用先**: Access 2013、Office 2013

グループまたはユーザーのオブジェクトまたはオブジェクト コンテナーに対する権限を取得します。

## <a name="syntax"></a>構文

*ReturnValue*  = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>戻り値

グループまたはユーザーが、そのオブジェクトに持つ権限を含むビットマスクを示す長整数型 ( **Long** ) の値を取得します。この値は、1 つ以上の [RightsEnum](rightsenum.md) 定数です。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*名前* |権限を設定するオブジェクトの名前を示すバリアント型 (**Variant**) の値を指定します。オブジェクト コンテナーの権限を取得する場合は、*Name* を Null 値に設定します。|
|*ObjectType* |権限を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。|
|*ObjectTypeId* |省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。|


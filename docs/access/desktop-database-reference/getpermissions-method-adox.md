---
title: getpermissions メソッド (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292245"
---
# <a name="getpermissions-method-adox"></a>getpermissions メソッド (ADOX)

**適用先:** Access 2013、Office 2013

グループまたはユーザーのオブジェクトまたはオブジェクト コンテナーに対する権限を取得します。

## <a name="syntax"></a>構文

*戻り* = ** ます。getpermissions (*Name*、 *ObjectType* \[、*objecttypeid*\])

## <a name="return-value"></a>戻り値

グループまたはユーザーが、そのオブジェクトに持つ権限を含むビットマスクを示す長整数型 ( **Long** ) の値を取得します。この値は、1 つ以上の [RightsEnum](rightsenum.md) 定数です。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*名前* |権限を設定するオブジェクトの名前を示すバリアント型 (**Variant**) の値を指定します。オブジェクト コンテナーの権限を取得する場合は、*Name* を Null 値に設定します。|
|*ObjectType* |権限を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。|
|*objecttypeid* |省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。|


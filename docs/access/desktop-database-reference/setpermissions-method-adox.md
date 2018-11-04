---
title: SetPermissions メソッド (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9ea1c08223282654af636326ba9a8c2bfe70e67
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949601"
---
# <a name="setpermissions-method-adox"></a>SetPermissions メソッド (ADOX)

**適用されます**Access 2013、Office 2013。

グループまたはユーザーのオブジェクトに対する権限を指定します。

## <a name="syntax"></a>構文

*<*。SetPermissions*名*、*オブジェクト タイプ*、*アクション*、ユーザーの*権利* \[、*継承*\] \[、*ObjectTypeId*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Name* |権限を設定するオブジェクトの名前を指定する文字列型 ( **String** ) の値。|
|*ObjectType* |**ObjectTypeEnum** 定数のいずれかである長整数型 ( [Long](objecttypeenum.md) ) の値。権限を与えるオブジェクトの種類を指定します。|
|*Action* |**ActionEnum** 定数のいずれかである長整数型 ( [Long](actionenum.md) ) の値。権限を設定するときに実行するアクションの種類を指定します。|
|*Rights* |1 つ以上の **RightsEnum** 定数のビットマスクである長整数型 ( [Long](rightsenum.md) ) の値。設定する権限を示します。|
|*Inherit* |省略可能です。**InheritTypeEnum** 定数のいずれかである長整数型 ( [Long](inherittypeenum.md) ) の値。オブジェクトによるこれらの権限の継承方法を指定します。既定値は **adInheritNone** です。|
|*ObjectTypeId* |省略可能。 OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。 **AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。|

## <a name="remarks"></a>解説

プロバイダーがグループまたはユーザーのアクセス権の設定をサポートしていない場合は、エラーが発生します。

> [!NOTE]
> **SetPermissions**を呼び出すときにアクションを**adAccessRevoke**に設定する*権限*のパラメーターの設定をオーバーライドします。 *Rights*パラメーターで指定されている権限を有効にする場合、*アクション*を**adAccessRevoke**に設定しないでください。



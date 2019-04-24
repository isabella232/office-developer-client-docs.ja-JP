---
title: SetPermissions メソッド (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314582"
---
# <a name="setpermissions-method-adox"></a>SetPermissions メソッド (ADOX)

**適用先:** Access 2013、Office 2013

グループまたはユーザーのオブジェクトに対する権限を指定します。

## <a name="syntax"></a>構文

*grouporuser*。SetPermissions*Name*、 *ObjectType*、 *Action*、 *Rights* \[、*Inherit* \] \[、*objecttypeid*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Name* |権限を設定するオブジェクトの名前を指定する文字列型 ( **String** ) の値。|
|*ObjectType* |**ObjectTypeEnum** 定数のいずれかである長整数型 ( [Long](objecttypeenum.md) ) の値。権限を与えるオブジェクトの種類を指定します。|
|*Action* |**ActionEnum** 定数のいずれかである長整数型 ( [Long](actionenum.md) ) の値。権限を設定するときに実行するアクションの種類を指定します。|
|*Rights* |1 つ以上の **RightsEnum** 定数のビットマスクである長整数型 ( [Long](rightsenum.md) ) の値。設定する権限を示します。|
|*Inherit* |省略可能です。**InheritTypeEnum** 定数のいずれかである長整数型 ( [Long](inherittypeenum.md) ) の値。オブジェクトによるこれらの権限の継承方法を指定します。既定値は **adInheritNone** です。|
|*objecttypeid* |省略可能です。OLE DB 仕様によって定義されていないプロバイダー オブジェクトの種類の GUID を示すバリアント型 (**Variant**) の値を指定します。このパラメーターは、*ObjectType* が **adPermObjProviderSpecific** に設定されている場合に必要です。その他の場合は使用されません。|

## <a name="remarks"></a>注釈

プロバイダーがグループまたはユーザーのアクセス権の設定をサポートしていない場合は、エラーが発生します。

> [!NOTE]
> **SetPermissions** を呼び出すときに、Actions を **adAccessRevoke** に設定すると、*Rights* パラメーターのすべての設定が無効になります。*Rights* パラメーターで指定した権限を有効にする場合は、*Actions* を **adAccessRevoke** に設定しないでください。



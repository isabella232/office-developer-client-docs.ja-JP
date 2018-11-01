---
title: SetPermissions メソッド (ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 433ddcc0394ff3543cd47b6399cb430890972920
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889526"
---
# <a name="setpermissions-method-adox"></a>SetPermissions メソッド (ADOX)


**適用されます**Access 2013、Office 2013。



グループまたはユーザーのオブジェクトに対する権限を指定します。

## <a name="syntax"></a>構文

*<*。SetPermissions*名*、*オブジェクト タイプ*、*アクション*、ユーザーの*権利* \[、*継承*\] \[、*ObjectTypeId*\]

## <a name="parameters"></a>パラメーター

  - *Name*

  - 権限を設定するオブジェクトの名前を指定する文字列型 ( **String** ) の値。

  - *ObjectType*

  - **ObjectTypeEnum** 定数のいずれかである長整数型 ( [Long](objecttypeenum.md) ) の値。権限を与えるオブジェクトの種類を指定します。

  - *Action*

  - **ActionEnum** 定数のいずれかである長整数型 ( [Long](actionenum.md) ) の値。権限を設定するときに実行するアクションの種類を指定します。

  - *Rights*

  - 1 つ以上の **RightsEnum** 定数のビットマスクである長整数型 ( [Long](rightsenum.md) ) の値。設定する権限を示します。

  - *Inherit*

  - 省略可能です。**InheritTypeEnum** 定数のいずれかである長整数型 ( [Long](inherittypeenum.md) ) の値。オブジェクトによるこれらの権限の継承方法を指定します。既定値は **adInheritNone** です。

  - *ObjectTypeId*

  - 省略可能。 OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。 **AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。

## <a name="remarks"></a>解説

プロバイダーがグループまたはユーザーのアクセス権の設定をサポートしていない場合は、エラーが発生します。


> [!NOTE]
> <P><STRONG>SetPermissions</STRONG>を呼び出すときにアクションを<STRONG>adAccessRevoke</STRONG>に設定する<EM>権限</EM>のパラメーターの設定をオーバーライドします。 <EM>Rights</EM>パラメーターで指定されている権限を有効にする場合、<EM>アクション</EM>を<STRONG>adAccessRevoke</STRONG>に設定しないでください。</P>



---
title: GetPermissions メソッド (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f53298d56f09b3df94c1b9e20158b3549317af6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886537"
---
# <a name="getpermissions-method-adox"></a>GetPermissions メソッド (ADOX)


**適用されます**Access 2013、Office 2013。


グループまたはユーザーのオブジェクトまたはオブジェクト コンテナーに対する権限を取得します。

## <a name="syntax"></a>構文

*戻り値* = *<*。GetPermissions (*名前*、 *ObjectType* \[、*ObjectTypeId*\])

## <a name="return-value"></a>戻り値

グループまたはユーザーが、そのオブジェクトに持つ権限を含むビットマスクを示す長整数型 ( **Long** ) の値を取得します。この値は、1 つ以上の [RightsEnum](rightsenum.md) 定数です。

## <a name="parameters"></a>パラメーター

  - *Name*

  - 権限を設定するオブジェクトの名前を示すバリアント型 ( **Variant** ) の値を指定します。 オブジェクト コンテナーの権限を取得する場合は、null 値に*名前*を設定します。

  - *ObjectType*

  - 権限を取得するオブジェクトの種類を示す、**ObjectTypeEnum** 定数の 1 つである長整数型 ( [Long](objecttypeenum.md) ) の値を指定します。

  - *ObjectTypeId*

  - 省略可能。 OLE DB 仕様で定義されていないプロバイダーのオブジェクト型の GUID を指定する**バリアント型**の値です。 **AdPermObjProviderSpecific**; に*オブジェクト タイプ*が設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。


---
title: ChangePassword メソッド (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296529"
---
# <a name="changepassword-method-adox"></a>ChangePassword メソッド (ADOX)

**適用先:** Access 2013、Office 2013

ユーザー アカウントのパスワードを変更します。

## <a name="syntax"></a>構文

*ユーザー*。ChangePassword*oldpassword*, *NewPassword*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*oldpassword* |ユーザーの現在のパスワードを示す文字列型 ( **String** ) の値を指定します。 ユーザーが現在パスワードを使用していない場合は、*OldPassword* に空の文字列 ("") を指定してください。|
|*NewPassword* |新しいパスワードを表す文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

セキュリティ上の理由から、新規パスワードに加え、古いパスワードを指定する必要があります。

プロバイダーがトラスティ プロパティの管理をサポートしていない場合は、エラーが発生します。


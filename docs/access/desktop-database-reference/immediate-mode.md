---
title: イミディ エイト モード (デスクトップ データベース参照のアクセス)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6401e7954325eded85b70b9edb5d164e857d113
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947862"
---
# <a name="immediate-mode"></a>イミディ エイト モード


**適用されます**Access 2013、Office 2013。

イミディエイト モードは、 **LockType** プロパティが **adLockOptimistic** または **adLockPessimistic** に設定されているときに有効になります。イミディエイト モードでは、 **Update** メソッドを呼び出すことによって、行に対する操作が完了したことを宣言すると直ちにレコードに対する変更が通知されます。

## <a name="calling-update"></a>Update を呼び出す

**Update** メソッドを呼び出す前に、追加または編集中のレコードから移動すると、ADO によって **Update** が自動的に呼び出され、変更が保存されます。現在のレコードに対する変更を取り消す場合や、新しく追加したレコードを破棄する場合は、移動する前に **CancelUpdate** メソッドを呼び出す必要があります。

現在のレコードは、 **Update** メソッドの呼び出し後も現在のレコードのままです。

## <a name="cancelupdate"></a>CancelUpdate

**CancelUpdate** メソッドを使用すると、現在の行に対する変更を取り消したり、新しく追加した行を破棄したりできます。 **Update** メソッドを呼び出した後は、現在のレコードに対する変更や新しい行を取り消すことができません。ただし、変更が **RollbackTrans** メソッドによってロールバックできるトランザクションの一部である場合や、バッチ更新の一部である場合を除きます。バッチ更新の場合は、 **Update** を **CancelUpdate** メソッドまたは **CancelBatch** メソッドによって取り消すことができます。

**CancelUpdate** メソッドを呼び出したときに新しい行を追加している途中であった場合は、 **AddNew** を呼び出す前に現在の行であった行が現在の行になります。

現在の行を変更したり、新しい行を追加したりしていない場合に **CancelUpdate** メソッドを呼び出すと、エラーが生成されます。


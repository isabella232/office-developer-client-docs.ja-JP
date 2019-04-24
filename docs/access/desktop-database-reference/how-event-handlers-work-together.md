---
title: イベント ハンドラーの共同作業の方法
TOCTitle: How event handlers work together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e772e93f27d6bb5f30d865e3435d4bde6bdc5e73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291923"
---
# <a name="how-event-handlers-work-together"></a>イベント ハンドラーの共同作業の方法

**適用先:** Access 2013、Office 2013

Visual Basic でプログラミングするのでない限り、 **Connection** イベントと **Recordset** イベントのイベント ハンドラーは、それらのイベントを実際に処理するかどうかにかかわらず、すべて実装する必要があります。実装に必要な作業量は、使用するプログラミング言語によって異なります。詳細については、「 [ADO イベントのインスタンス化 (言語別)](https://docs.microsoft.com/office/client-developer/access/desktop-database-reference/ado-event-instantiation-by-language-ado)」を参照してください。

## <a name="paired-event-handlers"></a>ペアになったイベントハンドラー

各 Will イベント ハンドラーには、関連する Complete イベント ハンドラーがあります。たとえば、アプリケーションでフィールドの値を変更すると、 **WillChangeField** イベント ハンドラーが呼び出されます。変更を受け入れてもよい場合、アプリケーションで **adStatus** パラメーターを変更しないようにすると、操作が実行されます。操作が終了すると、 **FieldChangeComplete** イベントが操作の完了をアプリケーションに通知します。操作が正常に完了していれば、 **adStatus** に **adStatusOK** が格納されます。それ以外の場合は、 **adStatus** に **adStatusErrorsOccurred** が格納されるので、この場合は、アプリケーションで **Error** オブジェクトを調べて、エラーの原因を知る必要があります。

**WillChangeField** が呼び出されたときに、その変更操作が行われないようにする場合もあります。そのような場合は、 **adStatus** を **adStatusCancel** に設定します。操作はキャンセルされ、 **FieldChangeComplete** イベントは値 **adStatusErrorsOccurred** が設定された **adStatus** を受け取ります。操作がキャンセルされたことを **FieldChangeComplete** ハンドラーが判断できるように、 **Error** オブジェクトには **adErrOperationCancelled** が格納されています。ただし、 **adStatus** を **adStatusCancel** に設定しても、プロシージャのエントリでパラメーターが **adStatusCantDeny** に設定されていると、キャンセル操作は無効になるので、変更を行う前に **adStatus** の値を確認する必要があります。

Sometimes an operation can raise more than one event. For example, the **Recordset** object has paired events for **Field** changes and **Record** changes. When your application changes the value of a **Field**, the **WillChangeField** event handler is called. If it determines that the operation can continue, the **WillChangeRecord** event handler is also raised. If this handler also allows the event to continue, the change is made and the **FieldChangeComplete** and **RecordChangeComplete** event handlers are called. The order in which the Will event handlers for a particular operation are called is not defined, so you should avoid writing code that depends on calling handlers in a particular sequence.

複数の Will イベントが発生する状況では、そのうちの 1 つのイベントで、保留中の操作が取り消される可能性があります。たとえば、アプリケーションで **Field** の値を変更する場合、通常は、 **WillChangeField** イベント ハンドラーと **WillChangeRecord** イベント ハンドラーの両方が呼び出されます。しかし、最初に呼び出されたイベント ハンドラーで操作が取り消されると、それと対の Complete ハンドラーが **adStatusOperationCancelled** で呼び出されます。2 つ目のハンドラーは呼び出されません。これに対し、最初のイベント ハンドラーでイベントの続行が許可されると、2 つ目のイベント ハンドラーも呼びさ出されます。2 つ目のハンドラーで操作が取り消されると、前の例に示したように、対になる Complete イベントが 2 つとも呼び出されます。

## <a name="unpaired-event-handlers"></a>ペアになっていないイベントハンドラー

イベントに渡された状態が**adstatuscantdeny**でない限り、 *status*パラメーターで**adStatusUnwantedEvent**を返すことにより、任意のイベントのイベント通知をオフにすることができます。 For example, when your Complete event handler is called the first time, you can return **adStatusUnwantedEvent**. You will subsequently receive only Will events. However, some events can be triggered for more than one reason. その場合、イベントには*Reason*パラメーターが設定されます。 When you return **adStatusUnwantedEvent**, you will stop receiving notifications for that event only when they occur for that particular reason. In other words, you will potentially receive notification for each possible reason that the event could be triggered.

単一の Will イベント ハンドラーは、操作に使用するパラメーターの検証に便利です。このイベント ハンドラーで、操作パラメーターの変更または操作のキャンセルを行うことができます。

一方、Complete イベントによる通知を有効のままにしておく方法もあります。最初の Will イベント ハンドラーが呼び出されたときに、 **adStatusUnwantedEvent** を返します。それ以降は、Complete イベントのみを受け取るようになります。

単一の Complete イベント ハンドラーは、非同期操作の管理に便利です。非同期操作には、それぞれ適切な Complete イベントが関連付けられています。

たとえば、非常に大きな [Recordset](recordset-object-ado.md) オブジェクトへのデータの格納には時間がかかることがあります。 アプリケーションが適切に記述されている場合は、操作を開始して、他の処理を続行することができます。 **Recordset** へのデータ格納が完了したことは、 **ExecuteComplete** イベントの通知によって知るようにします。

## <a name="single-event-handlers-and-multiple-objects"></a>単一のイベントハンドラーと複数のオブジェクト

Microsoft Visual C++ のような柔軟性のあるプログラミング言語では、複数のオブジェクトからのイベントを 1 つのイベント ハンドラーで処理することができます。たとえば、複数の **Connection** オブジェクトからのイベントを 1 つの **Disconnect** イベント ハンドラーで処理できます。接続の 1 つが終了すると、 **Disconnect** イベント ハンドラーが呼び出されます。イベント ハンドラーのオブジェクト パラメーターが対応する **Connection** オブジェクトに設定されるため、どの接続がイベントを発生させたかを判別できます。

> [!NOTE]
> [!メモ] Visual Basic では 1 つのイベント ハンドラーに 1 つのオブジェクトしか関連付けできないため、この手法は Visual Basic では使用できません。



---
title: 複数のイベント ハンドラーとの共同作業
TOCTitle: How Event Handlers Work Together
ms:assetid: 02122824-881e-0bb8-cba1-c963024790ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248788(v=office.15)
ms:contentKeyID: 48542951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d156de0a794798be6f7e68925d934c07a28cd60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479113"
---
# <a name="how-event-handlers-work-together"></a>複数のイベント ハンドラーとの共同作業


**適用されます**Access 2013 |。Office 2013



Visual Basic でプログラミングするのでない限り、 **Connection** イベントと **Recordset** イベントのイベント ハンドラーは、それらのイベントを実際に処理するかどうかにかかわらず、すべて実装する必要があります。実装に必要な作業量は、使用するプログラミング言語によって異なります。詳細については、「 [ADO イベントのインスタンス化 (言語別)](https://msdn.microsoft.com/library/jj250244\(v=office.15\))」を参照してください。

## <a name="paired-event-handlers"></a>対のイベント ハンドラー

各 Will イベント ハンドラーには、関連する Complete イベント ハンドラーがあります。たとえば、アプリケーションでフィールドの値を変更すると、 **WillChangeField** イベント ハンドラーが呼び出されます。変更を受け入れてもよい場合、アプリケーションで **adStatus** パラメーターを変更しないようにすると、操作が実行されます。操作が終了すると、 **FieldChangeComplete** イベントが操作の完了をアプリケーションに通知します。操作が正常に完了していれば、 **adStatus** に **adStatusOK** が格納されます。それ以外の場合は、 **adStatus** に **adStatusErrorsOccurred** が格納されるので、この場合は、アプリケーションで **Error** オブジェクトを調べて、エラーの原因を知る必要があります。

**WillChangeField** が呼び出されたときに、その変更操作が行われないようにする場合もあります。そのような場合は、 **adStatus** を **adStatusCancel** に設定します。操作はキャンセルされ、 **FieldChangeComplete** イベントは値 **adStatusErrorsOccurred** が設定された **adStatus** を受け取ります。操作がキャンセルされたことを **FieldChangeComplete** ハンドラーが判断できるように、 **Error** オブジェクトには **adErrOperationCancelled** が格納されています。ただし、 **adStatus** を **adStatusCancel** に設定しても、プロシージャのエントリでパラメーターが **adStatusCantDeny** に設定されていると、キャンセル操作は無効になるので、変更を行う前に **adStatus** の値を確認する必要があります。

1 つの操作から複数のイベントが発生することもあります。たとえば、Recordset オブジェクトには、Field 変更と Record 変更に関する対をなすイベントがあります。アプリケーションで Field の値を変更すると、WillChangeField イベント ハンドラーが呼び出されます。WillChangeField イベント ハンドラーで、その操作を続行できると決定した場合、さらに WillChangeRecord イベント ハンドラーが起動します。WillChangeRecord イベント ハンドラーでもイベントの続行が許可されると、変更操作が実行され、FieldChangeComplete イベント ハンドラーと RecordChangeComplete イベント ハンドラーが呼び出されます。個々の操作に対する Will イベント ハンドラー群の呼び出し順序は定義されていないので、ハンドラーの特定の呼び出し順序に依存するコードは記述しないでください。

複数の Will イベントが発生する状況では、そのうちの 1 つのイベントで、保留中の操作が取り消される可能性があります。たとえば、アプリケーションで **Field** の値を変更する場合、通常は、 **WillChangeField** イベント ハンドラーと **WillChangeRecord** イベント ハンドラーの両方が呼び出されます。しかし、最初に呼び出されたイベント ハンドラーで操作が取り消されると、それと対の Complete ハンドラーが **adStatusOperationCancelled** で呼び出されます。2 つ目のハンドラーは呼び出されません。これに対し、最初のイベント ハンドラーでイベントの続行が許可されると、2 つ目のイベント ハンドラーも呼びさ出されます。2 つ目のハンドラーで操作が取り消されると、前の例に示したように、対になる Complete イベントが 2 つとも呼び出されます。

## <a name="unpaired-event-handlers"></a>対でないイベント ハンドラー

としてイベントに渡されるステータスが**adStatusCantDeny**ではありません、*状態*パラメーターに**adStatusUnwantedEvent**を返すことによって任意のイベントのイベント通知を無効にできます。 たとえば、完了イベント ハンドラーが呼び出されると最初に、 **adStatusUnwantedEvent**を返すことができます。 その後 Will イベントのみが表示されます。 ただし、理由の 1 つ以上のいくつかのイベントは発生します。 その場合は、イベントは、 *"理由*"パラメーターがあります。 **AdStatusUnwantedEvent**を返すとき、その特定の理由が発生したときにのみイベント通知の受信を停止します。 つまり、イベントが発生することを理由の通知が表示されます可能性があります。

単一の Will イベント ハンドラーは、操作に使用するパラメーターの検証に便利です。このイベント ハンドラーで、操作パラメーターの変更または操作のキャンセルを行うことができます。

一方、Complete イベントによる通知を有効のままにしておく方法もあります。最初の Will イベント ハンドラーが呼び出されたときに、 **adStatusUnwantedEvent** を返します。それ以降は、Complete イベントのみを受け取るようになります。

単一の Complete イベント ハンドラーは、非同期操作の管理に便利です。非同期操作には、それぞれ適切な Complete イベントが関連付けられています。

たとえば、非常に大きな [Recordset](recordset-object-ado.md) オブジェクトへのデータの格納には時間がかかることがあります。 アプリケーションが適切に書き込まれる場合、操作を開始し、他の処理を続行できます。 **Recordset** へのデータ格納が完了したことは、 **ExecuteComplete** イベントの通知によって知るようにします。

## <a name="single-event-handlers-and-multiple-objects"></a>単一のイベント ハンドラーと複数のオブジェクト

Microsoft Visual C++ のような柔軟性のあるプログラミング言語では、複数のオブジェクトからのイベントを 1 つのイベント ハンドラーで処理することができます。たとえば、複数の **Connection** オブジェクトからのイベントを 1 つの **Disconnect** イベント ハンドラーで処理できます。接続の 1 つが終了すると、 **Disconnect** イベント ハンドラーが呼び出されます。イベント ハンドラーのオブジェクト パラメーターが対応する **Connection** オブジェクトに設定されるため、どの接続がイベントを発生させたかを判別できます。


> [!NOTE]
> <P>[!メモ] Visual Basic では 1 つのイベント ハンドラーに 1 つのオブジェクトしか関連付けできないため、この手法は Visual Basic では使用できません。</P>



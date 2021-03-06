---
title: 'Xamarin.Essentials: 전화 걸기'
description: Xamarin.Essentials의 PhoneDialer 클래스를 사용하면 응용 프로그램이 전화 걸기에서 전화 번호를 열 수 있습니다.
ms.assetid: E7457942-4D7B-4195-A2FF-417919B9537F
author: jamesmontemagno
ms.author: jamont
ms.date: 11/04/2018
ms.openlocfilehash: 8d4b0cdcae5e33ac2c48baa0b7749597314eae8c
ms.sourcegitcommit: 01f93a34b466f8d4043cef68fab9b35cd8decee6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52898275"
---
# <a name="xamarinessentials-phone-dialer"></a>Xamarin.Essentials: 전화 걸기

**PhoneDialer** 클래스를 사용하면 응용 프로그램이 전화 걸기에서 전화 번호를 열 수 있습니다.

## <a name="get-started"></a>시작

[!include[](~/essentials/includes/get-started.md)]

## <a name="using-phone-dialer"></a>전화 걸기 사용

클래스에서 Xamarin.Essentials에 대한 참조를 추가합니다.

```csharp
using Xamarin.Essentials;
```

전화 걸기 기능은 전화 걸기를 열기 위해 전화 번호로 `Open` 메서드를 호출하여 작동합니다. `Open`이 요청되면 API는 국가 번호(지정된 경우)에 따라 자동으로 숫자 형식을 지정하려고 합니다.

```csharp
public class PhoneDialerTest
{
    public async Task PlacePhoneCall(string number)
    {
        try
        {
            PhoneDialer.Open(number);
        }
        catch (ArgumentNullException anEx)
        {
            // Number was null or white space
        }
        catch (FeatureNotSupportedException ex)
        {
            // Phone Dialer is not supported on this device.
        }
        catch (Exception ex)
        {
            // Other error has occurred.
        }
    }
}
```

## <a name="api"></a>API

- [전화 걸기 소스 코드](https://github.com/xamarin/Essentials/tree/master/Xamarin.Essentials/PhoneDialer)
- [전화 걸기 API 문서](xref:Xamarin.Essentials.PhoneDialer)

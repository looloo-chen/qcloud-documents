## 简介

弹性公网 IP（EIP），是与账号关联的静态 IP 地址。弹性公网 IP 未进行释放前， 您可以将其一直保留于您的账号中。 相较于公网 IP 仅可跟随云服务器一起申请释放，弹性公网 IP 可以与云服务器的生命周期解耦，作为云资源单独进行操作。

例如，若您需要保留某个与业务强相关的公网IP，可以将其转为弹性公网IP保留在您的账号中。

## 规则与限制

### 使用规则

- 弹性 IP 地址同时适用于基础网络和私有网络的实例，以及私有网络中的 [NAT 网关](https://cloud.tencent.com/document/product/215/20079) 实例。
- 弹性 IP 地址与腾讯云账户相关联，而不是与某个具体实例相关联。
- 当您选择、释放弹性 IP 地址，弹性公网 IP 绑定的包年包月主机欠费超过7天未续费，或者账号欠费超过26小时之前，弹性 IP 地址均会与腾讯云账户一直保持关联。
- 将弹性 IP 地址与实例绑定时，实例的当前公网 IP 地址会释放到基础网络公网 IP 地址池中。如果弹性 IP 地址与实例在解绑时选择了重新分配公网 IP ，实例会自动分配到新的公网 IP 地址（无法保证与绑定前的公网 IP 一致）。此外，销毁实例也会与弹性 IP 地址断开关联。
 
### 使用限制

- 每个腾讯云账户每个地域每天申购次数为**配额数\*2**次。
- 每个腾讯云账户每个地域下最多可创建**20**个弹性公网 IP。
- 解绑 EIP 时，可免费重新分配公网 IP 的次数为**每个腾讯云账户每天10次**。
- **1个弹性公网 IP 同一时间只能绑定到1个 CVM/NAT 网关实例上**，支持动态的绑定和解绑。

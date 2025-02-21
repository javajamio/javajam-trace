# JavaJAM State Transition Traces

ASN.1 Schema
```
OpaqueHash ::= OCTET STRING (SIZE(32))
ByteSequence ::= OCTET STRING

TestCase ::= SEQUENCE {
    pre_state    TestState,
    block        Block,
    post_state   TestState
}

TestState ::= SEQUENCE {
    state_root   OpaqueHash,
    keyvals      KeyVals
}

KeyVals ::= SEQUENCE OF KeyVal
KeyVal ::= SEQUENCE (SIZE(4)) OF ByteSequence
```

All transition vectors are based on the [Tiny](https://docs.jamcha.in/basics/chain-spec/tiny) chain specifications.
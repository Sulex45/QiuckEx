# Partial Payment Support — Implementation TODO

## Steps

- [x] 1. Update `types.rs` — add `amount_paid` to `EscrowEntry` and `PrivacyAwareEscrowView`
- [x] 2. Update `errors.rs` — add `Overpayment` and `NotFullyPaid` error codes
- [x] 3. Update `events.rs` — add `EscrowPartialPaymentEvent`, `EscrowFinalizedEvent`, and publish helpers
- [x] 4. Update `escrow.rs` — core logic: `create_payment_request`, `partial_pay`, update `deposit`, `deposit_with_commitment`, `withdraw`, `refund`, `resolve_dispute`
- [x] 5. Update `lib.rs` — expose new contract methods, update `get_escrow_details`
- [x] 6. Update `test.rs` — fix all `EscrowEntry` constructions, add new partial-payment tests
- [x] 7. Update `bench_test.rs` — fix `EscrowEntry` constructions
- [x] 8. Update `storage_test.rs` — fix `EscrowEntry` constructions
- [x] 9. Update `storage.rs` — add `CreatePaymentRequest` and `PartialPay` to `PauseFlag`
- [ ] 10. Run `cargo test` and fix any compilation or test failures
- [ ] 11. Regenerate snapshots if necessary

## Notes

- Rust/Cargo is not installed on this Windows environment, so tests could not be executed locally.
- All code changes have been reviewed for consistency across the contract.
- To verify: open a terminal with Rust installed and run `cargo test` inside `app/contract/contracts/quickex`.

